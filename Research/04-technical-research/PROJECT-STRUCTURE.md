# Poetry in Motion: Project Structure

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Living document, Phase 1 technical foundation
Scope: How the repository is organised today; layered architecture; mapping from research to code
Cross-reference: 00-foundation/FOUNDATION.md, 01-global/LANDSCAPE.md, 04-technical-research/OPEN-SOURCE-REFERENCE.md
Last updated: May 2026

---

## Notation

Claims are tagged as follows.

- [VALIDATED]: Verified in the repository. File exists and route responds in development.
- [IMPLEMENTED]: Present as prototype or mock. Not production-hardened.
- [HYPOTHESIS]: Design intent not yet built.
- [RESEARCH DIRECTION]: Identified for a later phase.

---

## Section 1: Research-to-Code Map

Phase 1 flows from history through structure to future implementation.

| Research layer | Document | Code expression |
|----------------|----------|-----------------|
| Why we exist | 00-foundation/FOUNDATION.md | Copy, quiz fields, creator and circular modules |
| Industry context | 01-global/LANDSCAPE.md | Feature priorities: personalisation, marketplace, circular |
| Geographic context | 02-africa/ | Kenya-first payments, logistics, creator onboarding |
| Entity landscape | 03-market-intelligence/ENTITIES.md | Competitor differentiation, payment and logistics partners |
| System shape | This document | Folders, API domains, data types |

---

## Section 2: Repository Layout

```
poetry-in-motion/
  Research/                    (Phase 1 foundation, not shipped to end users)
    00-foundation/
    01-global/
    02-africa/
    03-market-intelligence/
    04-technical-research/
    05-critical-review/
    06-mvp/
  app/                         (Next.js App Router: pages and API)
  components/                  (UI and mobile-specific components)
  lib/                         (types, mock-data, utilities, analytics helpers)
  public/                      (static assets, PWA manifest, service worker)
  package.json                 [RESEARCH DIRECTION] rename from my-v0-project
```

Stack [VALIDATED]: Next.js 15.2.4, React 19, Tailwind 4, pnpm, TypeScript.

---

## Section 3: Five-Layer Architecture (Target Model)

Industrial e-commerce history (01-global/LANDSCAPE.md Part 1) separates discovery, transaction, fulfillment, and data. Poetry in Motion maps these into five layers. Today Layers 1 through 3 are largely mock. Layers 4 and 5 are skeletal.

```
Layer 5: Experience and Community
Live sessions, referrals, testimonials, notifications

Layer 4: Trust, Circular, and Sustainability
Trade-in, pre-owned, impact metrics, verified creators

Layer 3: Personalisation and AI
Quiz, style profile, recommendations, image analysis

Layer 2: Commerce Core
Catalog, cart, orders, subscriptions, payments

Layer 1: Identity and Data
Auth, users, analytics events, search index
```

### Layer 1: Identity and Data [IMPLEMENTED] mock

| Concern | Routes and files | Production gap |
|---------|-----------------|----------------|
| Auth | app/api/auth/login, signup | No password hash; base64 token |
| Users | app/api/users/[id], lib/types.ts User | No database |
| Analytics | app/api/analytics/events, lib/analytics.ts | No warehouse |
| Search | app/api/search/* | No index engine |

Historical anchor: Amazon account and order history; GDPR-era consent (Phase 4).

### Layer 2: Commerce Core [IMPLEMENTED] mock

| Concern | Routes and files | Production gap |
|---------|-----------------|----------------|
| Catalog | app/api/products/*, app/shop/* | Mock mockProducts only |
| Cart and orders | app/api/cart, orders/* | No payment PSP (M-Pesa, card) |
| Subscriptions | app/api/subscriptions/* | No billing |
| Favorites | app/api/favorites | No persistence |

Historical anchor: Shopify enablement and checkout; Africa COD and mobile money (01-global/LANDSCAPE.md section 2.7 and 02-africa/KENYA.md).

### Layer 3: Personalisation and AI [IMPLEMENTED] mock

| Concern | Routes and files | Production gap |
|---------|-----------------|----------------|
| Style quiz | app/quiz/page.tsx | Client-only; not persisted to API |
| Style profile | app/api/style-profile | Mock linkage |
| Recommendations | app/api/recommendations/*, app/recommendations | Rule-based mock, not ML |
| AI | app/api/ai/*, app/ai/image-upload | Hard-coded analysis JSON |

Historical anchor: Stitch Fix quiz loop; modern vision APIs [RESEARCH DIRECTION].

### Layer 4: Trust, Circular, and Sustainability [IMPLEMENTED] mock UI

| Concern | Routes and files | Production gap |
|---------|-----------------|----------------|
| Circular UX | app/circular/page.tsx | Mock impact numbers |
| Trade-in | app/api/trade-in/* | No logistics partner |
| Pre-owned | app/api/pre-owned | No authentication of goods |
| Sustainability | app/api/sustainability/impact, product sustainability type | No supply-chain feed |
| Creators | app/creators, app/api/creators/* | No payouts or KYC |

Historical anchor: ThredUp and resale; EU sustainability reporting pressure (01-global/LANDSCAPE.md sections 1.6 and 2.5).

### Layer 5: Experience and Community [IMPLEMENTED] partial

| Concern | Routes and files | Production gap |
|---------|-----------------|----------------|
| Community | app/api/community/* | Mock |
| Referrals | app/referrals, app/api/referrals/* | No attribution ledger |
| Live | app/community/live-sessions | No WebRTC or stream vendor |
| Support | app/support, app/api/support/tickets/* | No ticketing integration |

Historical anchor: TikTok and Instagram social commerce; live shopping (01-global/LANDSCAPE.md section 2.6).

---

## Section 4: App Router Structure [VALIDATED]

### 4.1 Marketing and Product Pages

| Route | Layer | Role |
|-------|-------|------|
| / | 3, 5 | Positioning, feature narrative |
| /quiz | 3 | Onboarding and style capture |
| /shop, /shop/[id] | 2 | Transaction discovery |
| /dashboard | 1, 3 | Post-login hub |
| /recommendations | 3 | Personalised feed |
| /creators | 4, 5 | Creator economy |
| /circular | 4 | Circular fashion story and flows |
| /referrals | 5 | Growth |
| /analytics | 1 | User or admin analytics views |
| /ai/image-upload | 3 | Vision-style input |
| /pricing, /support, /security, /privacy, /terms | 2, 4 | Trust and compliance shell |
| /offline | 5 | PWA offline |
| /testimonials | 5 | Social proof |

### 4.2 API Surface (45 Route Handlers) [VALIDATED]

All [IMPLEMENTED] as mocks unless noted.

- auth (2), users (1), products (4), cart (1), orders (2)
- recommendations (3), ai (3), style-profile (1)
- creators (2), collections (3), pre-owned (1)
- trade-in (2), sustainability (1), subscriptions (2)
- referrals (2), favorites (1), search (2)
- community (8), support (2), analytics (1)

Pattern: handlers import lib/mock-data.ts or return static JSON. Comments reference future database.

---

## Section 5: Data Model [VALIDATED]

Source of truth for types: lib/types.ts. Mock instances: lib/mock-data.ts.

| Entity | Key relationships | Research pillar |
|--------|-------------------|-----------------|
| User | Style attributes, orders | Personalisation, representation |
| Product | creatorId, sustainability | Commerce, transparency |
| Creator | collections[] | Creator economy |
| Collection | products[], votes, status lifecycle | Community demand signalling |
| Order | items, shippingAddress | Industrial e-commerce core |
| TradeIn | userId, productId, condition | Circular fashion |

Collection lifecycle (draft, voting, production, available) [IMPLEMENTED] in types. Maps to 01-global/LANDSCAPE.md section 2.3 scarcity and drop logic, ethically reframed.

---

## Section 6: Components and Cross-Cutting Concerns

| Area | Location | Notes |
|------|----------|-------|
| Design system | components/ui/*, components.json | shadcn and Radix pattern |
| Mobile UX | components/mobile-* | Aligns with LANDSCAPE mobile-commerce era |
| Theming | theme-provider, theme-toggle | Dark and light |
| PWA | public/manifest.json, public/sw.js | [IMPLEMENTED] basic |
| Performance helpers | lib/performance.ts | [RESEARCH DIRECTION] expand with RUM |

Branding debt: UI strings still say StyleAI. Product name Poetry in Motion is a [RESEARCH DIRECTION] rename in Phase 2.

---

## Section 7: Phase Boundaries (Engineering)

| Phase | Research | Engineering focus | Data reality |
|-------|----------|-------------------|--------------|
| Phase 1 (current) | History, structure, critical review, MVP definition | Prototype frozen except Research folder | mock-data.ts |
| Phase 2 | ENTITIES.md extensions, competitors, payments | DB, auth, M-Pesa, rename brand in UI | Postgres or equivalent |
| Phase 3 | Deep dives: AI ethics, supply chain | Real recommendations, verified sustainability | External APIs |
| Phase 4 | Compliance, operations | Scale, monitoring, legal | Production SLAs |

Hard rule: Phase 2 does not claim verified sustainability in production until Layer 4 has auditable data sources.

---

## Section 8: Statistics [VALIDATED] (Audit Snapshot)

| Metric | Value |
|--------|-------|
| API route files | 45 |
| Page routes | 19 |
| Approximate total lines (non-git) | Approximately 20,600 |
| Mock product SKUs | 3 |
| Mock creators | 2 |

---

## Section 9: Phase 1 Exit Checklist

- [x] Historical e-commerce foundation documented (01-global/LANDSCAPE.md)
- [x] Fashion and e-commerce thread documented (01-global/LANDSCAPE.md Part 2)
- [x] Geographic narrowing documented: Africa, East Africa, Kenya (02-africa/)
- [x] Layered project structure mapped to repository (this document)
- [x] Foundation narrative in 00-foundation/FOUNDATION.md
- [x] Entity landscape documented (03-market-intelligence/ENTITIES.md)
- [x] Critical review written (05-critical-review/CRITICAL-REVIEW.md)
- [ ] MVP wedge defined (06-mvp/MVP.md)
- [ ] Retire StyleAI label in application code
- [ ] Rename package.json name to poetry-in-motion

---

## References

- Repository paths under app/, lib/, components/
- 01-global/LANDSCAPE.md: normative constraints on structure
- 03-market-intelligence/ENTITIES.md: competitor and partner landscape
- 04-technical-research/OPEN-SOURCE-REFERENCE.md: technical options
