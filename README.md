# SparkForge

**The ultimate open-source ERP · CRM · CMS · Martech stack.**

> Forge the definitive business platform from free-as-in-beer tools, Drupal 11 headless power, Puck visual editing, and Atomic Design discipline.

**Status:** v0.1 — Blueprint & Arsenal Tracker  
**Owner:** Lee Quessenberry (`lquessenberry`)  
**License:** MIT (core) + component-specific licenses

---

## Vision

SparkForge is the living catalog, architecture, and implementation plan for the most powerful, fully-owned, zero-vendor-lock-in business operating system possible:

- **CMS** — Drupal 11 (recipes, SDC, GraphQL, Entity API, Webforms)
- **Commerce / ERP core** — Drupal Commerce + Entity API
- **CRM & Martech** — self-hosted (n8n, PostHog, Mautic-style flows, Sparky AI)
- **Visual Builder** — Puck extended with nesting, grids, and fully granular aBEM components
- **Frontend** — Astro / Next.js decoupled, design-token driven
- **Arsenal** — continuous stash of the best free npm/OSS replacements for paid SaaS

We already have working prototypes. This repo is the **meta-layer** that unifies them, tracks the free tools, and drives the next iterations.

---

## Name & Mark

**SparkForge**  
*Spark* = the Simple Spark / Spark Nexus lineage (Sparky AI, Spark-Shop, Spark Nexus).  
*Forge* = the act of forging the ultimate stack from raw free tools and battle-tested prototypes.

**Logo concept (v0.1):**  
A stylized anvil + single bright spark, overlaid on a modular grid (hinting at Puck grids + aBEM atoms). Color: deep charcoal + electric amber/yellow spark (brand yellow from Spark Nexus work).  
*Placeholder SVG will live in `/assets/logo/` — generate next.*

---

## Core Stack Assumptions (v0.1)

| Layer | Choice | Notes |
|-------|--------|-------|
| Backend | Drupal 11 on **DDEV** | Recipes, SDC, GraphQL, Entity API, Webforms API, Commerce API |
| Decoupled Frontend | Astro + Puck (or Next.js) | Existing `puck-bem-atomic-nextjs` + `spark-nexus` |
| Component System | **aBEM** (Atomic Block Element Modifier) | Strict BEM + Atomic Design + Subatomic tokens |
| Visual Editor | Puck | **Extend** with nesting, CSS Grid / flex grids, draggable section controls, fully editable attributes |
| Commerce | Drupal Commerce | Default |
| Automation / Martech | n8n + PostHog + Sparky | Self-hosted free |
| Design Tokens | Style Dictionary + SCSS modules | From `dsforge` + `noyes-rand-ts` experiments |
| Hosting | Fly.io (proven) | Matches Axanar, Spark-Shop, etc. |

---

## Existing Prototypes (Review & Absorb)

These repos already contain pieces of the plan. SparkForge will reference, extract patterns from, and eventually unify them:

| Repo | Relevance |
|------|-----------|
| [`puck-bem-atomic-nextjs`](https://github.com/lquessenberry/puck-bem-atomic-nextjs) | **Primary Puck + aBEM + Atomic starter**. Subatomic tokens, organisms, SCSS modules. Roadmap already calls for section composition. |
| [`spark-nexus`](https://github.com/lquessenberry/spark-nexus) | Drupal 11 Headless + Astro + n8n Martech platform. RFP pilots, member portals, self-hosted CRM. |
| [`Spark-Shop`](https://github.com/lquessenberry/Spark-Shop) | White-label POD + Puck + Printful + Snipcart + commission engine. |
| [`Drupal-Nexus`](https://github.com/lquessenberry/Drupal-Nexus) | Drupal 11 MarTech with HubSpot patterns (to be replaced by free stack). |
| [`axanar-decoupled`](https://github.com/lquessenberry/axanar-decoupled) | Production decoupled Drupal + Next.js on Fly.io. |
| [`hoffman`](https://github.com/lquessenberry/hoffman) | Decoupled Drupal Commerce storefront. |
| [`dsforge`](https://github.com/lquessenberry/dsforge) | Design-system extraction & rebuild tooling. |
| [`noyes-rand-ts`](https://github.com/lquessenberry/noyes-rand-ts) | Strict corporate modernism / grid / token design system. |

---

## Puck Extension Goals (v0.1 Priority)

Current `puck-bem-atomic-nextjs` is strong on atoms/molecules/organisms. Next steps for SparkForge:

1. **Nesting** — full support for nested Puck zones / components inside organisms.
2. **Grids** — first-class CSS Grid & Flexbox layout components with visual controls (columns, gap, alignment).
3. **Draggable Sections** — section-level reordering + grid-area controls inside the editor.
4. **Granular Attributes** — every aBEM element exposes editable attributes (data-*, ARIA, custom props) in the Puck sidebar.
5. **SDC Bridge** — map Drupal Single Directory Components ↔ Puck blocks so content editors and developers stay in sync.

---

## Free Tool Arsenal (Initial Stash)

Curated free-as-in-beer replacements for paid tools. Continuously expanded.

### Analytics & Product
- `posthog-js` + PostHog (self-host or free tier) → Mixpanel / Amplitude / Hotjar
- Plausible tracker

### Auth
- Better Auth / SuperTokens / Keycloak / Lucia / Auth.js → Auth0 / Clerk / Okta

### Automation
- n8n (self-hosted) → Zapier / Make

### API Clients
- Bruno / Hoppscotch → Postman

### CMS / Headless
- Strapi (or pure Drupal) → Contentful / Sanity

### Charts
- Chart.js / Recharts / Nivo / visx → Highcharts paid

### Forms
- react-hook-form + Zod / Valibot

### Search
- Meilisearch → Algolia

### Error Monitoring
- Self-hosted Sentry or lighter OSS

*(Full living list will live in `/arsenal/` as YAML or Markdown catalogs.)*

---

## v0.1 Deliverables

- [x] Repo created with vision & naming
- [x] Link & review existing prototypes
- [x] Initial free-tool arsenal seeded from research
- [ ] Logo SVG + favicon set
- [ ] `/docs/architecture-v0.1.md` — high-level diagram + data flow
- [ ] `/arsenal/index.md` — structured tool tracker
- [ ] Puck extension spike: nested zones + grid component in a feature branch of `puck-bem-atomic-nextjs`
- [ ] Drupal recipe skeleton that wires GraphQL + Commerce + Webforms + SDC for SparkForge
- [ ] Decision log for aBEM naming conventions across Puck + SDC

---

## How to Contribute / Iterate

1. Stash a new free tool → open an issue or PR to `/arsenal/`.
2. Prototype a Puck extension → branch from `puck-bem-atomic-nextjs` and link here.
3. Architecture decisions → add to `/docs/`.
4. This is the single source of truth for the “ultimate stack” plan.

---

**SparkForge** — Free tools. Strict architecture. Total ownership.

*Built on the shoulders of Simple Spark, Decoupled.io, and years of Drupal + modern frontend work.*
