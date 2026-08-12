# SparkForge Plan — v0.1

**Date:** 2026-08-11  
**Goal:** Establish the living blueprint and free-tool arsenal for the ultimate ERP/CRM/CMS/Martech platform.

## 1. Naming & Branding

- **Name:** SparkForge
- **Rationale:** Continues the Spark lineage (Spark Nexus, Spark-Shop, Sparky, Simple Spark) while adding the industrial “forge” metaphor for assembling a complete business OS from free components.
- **Logo direction:** Anvil + single spark over a modular grid. Charcoal + amber/yellow. SVG + PNG set in `/assets/logo/`.

## 2. Architecture Principles

1. **Own everything that matters** — prefer self-hosted or pure open-source over SaaS free tiers that can change.
2. **Drupal as the system of record** — Entity API, Commerce, Webforms, recipes, SDC.
3. **Puck as the visual control plane** — extended for real layout power (nesting, grids, section drag).
4. **aBEM everywhere** — Atomic Design + BEM namespacing + subatomic tokens. No hard-coded values in components.
5. **GraphQL as the contract** between Drupal and Astro/Next frontends.
6. **DDEV first** for local fidelity.

## 3. Immediate Workstreams

### A. Arsenal Tracker
- Create structured catalog of free npm/OSS tools that replace paid ones.
- Categories: Analytics, Auth, Automation, Charts, Forms, Search, Monitoring, Email, CMS alternatives, etc.
- Each entry: package name, replaces, license, self-host notes, npm link, status (evaluated / adopted / candidate).

### B. Puck Power-Ups
- Spike nested zones.
- First-class Grid component (columns, gap, justify/align, responsive breakpoints) with visual controls.
- Draggable section reordering + grid-area assignment.
- Attribute editor for every aBEM element (data attributes, ARIA, custom props).
- Bridge pattern: SDC ↔ Puck block so content and code stay synchronized.

### C. Drupal Recipe Skeleton
- Recipe that enables:
  - GraphQL + GraphQL Compose (or equivalent)
  - Commerce
  - Webforms + Webform GraphQL
  - SDC
  - Entity API patterns needed for CRM-like objects
- Document the aBEM ↔ SDC naming map.

### D. Prototype Unification
- Extract best patterns from:
  - `puck-bem-atomic-nextjs` (component architecture)
  - `spark-nexus` (martech + n8n + Astro)
  - `Spark-Shop` (commerce + commission + Puck)
  - `hoffman` + `axanar-decoupled` (production decoupled patterns)
- Decide what becomes the canonical starter for SparkForge v0.2.

## 4. Success Criteria for v0.1 Close

- [ ] Logo assets committed
- [ ] Arsenal has ≥ 20 high-quality free alternatives documented
- [ ] Architecture diagram (Mermaid or SVG) published
- [ ] One working Puck grid + nested component demo merged or linked
- [ ] Decision record for aBEM conventions published
- [ ] Clear next-step issues opened for v0.2 (recipe + full starter)

## 5. Out of Scope for v0.1

- Full production ERP modules
- Multi-tenant SaaS packaging
- Paid-tier integrations (we deliberately stay free/open)
- Mobile native apps

---

*Iterate ruthlessly. Stash liberally. Own the stack.*
