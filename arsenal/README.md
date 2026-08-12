# SparkForge Arsenal

Living catalog of free-as-in-beer npm packages and open-source tools that replace paid SaaS.

Add new discoveries here. Prefer tools that can be self-hosted or have truly unlimited free tiers.

## Format for New Entries

```yaml
- name: posthog-js
  replaces: Mixpanel, Amplitude, Hotjar
  category: analytics
  license: MIT
  self_host: true
  npm: https://www.npmjs.com/package/posthog-js
  notes: Full product analytics + session replay + feature flags. Primary recommendation.
  status: adopted
```

## Current Seed (from 2026-08 research)

### Analytics & Product Insights
- **posthog-js** + PostHog → Mixpanel / Amplitude / Hotjar
- Plausible tracker

### Authentication
- Better Auth
- SuperTokens
- Keycloak (JS adapters)
- Lucia
- Auth.js / NextAuth

### Automation / Workflows
- n8n (self-hosted unlimited)

### API Testing / Clients
- Bruno (Git-native)
- Hoppscotch

### Headless CMS Alternatives
- Strapi (when not using pure Drupal)

### Charts & Visualization
- Chart.js
- Recharts
- Nivo
- visx

### Forms
- react-hook-form + Zod / Valibot

### Search
- Meilisearch

### Error / Observability
- Self-hosted Sentry or lighter OSS alternatives

### Design Systems & Extraction
- Style Dictionary patterns (see `dsforge`)

---

*Keep this list growing. Every paid tool has a free path.*
