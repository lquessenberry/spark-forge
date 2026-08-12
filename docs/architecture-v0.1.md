# SparkForge Architecture — v0.1 Sketch

```mermaid
flowchart TB
    subgraph Editors
        Puck["Puck Editor<br/>(extended: nesting + grids + attributes)"]
        DrupalAdmin["Drupal Admin<br/>(recipes, SDC, Webforms)"]
    end

    subgraph Backend
        D11["Drupal 11<br/>Entity API · Commerce · GraphQL<br/>Webforms · Recipes · SDC"]
        n8n["n8n<br/>Automation / Martech"]
        PostHog["PostHog<br/>Product Analytics"]
    end

    subgraph Frontend
        Astro["Astro / Next.js<br/>aBEM Components<br/>Design Tokens"]
        Sparky["Sparky AI<br/>(optional Groq)"]
    end

    Puck -->|config + zones| Astro
    DrupalAdmin --> D11
    D11 -->|GraphQL| Astro
    D11 -->|webhooks / events| n8n
    Astro --> PostHog
    n8n --> PostHog
    Sparky --> Astro
```

## Key Contracts

1. **GraphQL** is the primary read/write contract between Drupal and the decoupled frontend.
2. **Puck config** is the source of truth for visual layout; SDC provides the Drupal-side component mirror.
3. **aBEM** naming is enforced in both Puck blocks and SDC templates.
4. **Events** from Commerce / Webforms / Entities flow into n8n for martech automation.
5. **PostHog** (or Plausible) captures product analytics without third-party SaaS dependency.

## Local Development

- DDEV for Drupal
- `npm run dev` for Astro/Puck frontend
- Optional Docker Compose for full stack (n8n + PostHog + frontend)

## Next Architecture Iterations

- Detailed entity model for CRM objects
- Commerce order + subscription flows mapped to n8n
- Token universe system (light/dark/brand) fully documented
- Fly.io multi-service topology
