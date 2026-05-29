# Poetry in Motion: MVP Definition

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Phase 1 apex document. Defines the Phase 2 engineering starting point.
Cross-reference: All Phase 1 documents. This document is the output of the pyramid.
Last updated: May 2026

---

## Purpose

Every layer of the Phase 1 research pyramid exists to justify one decision: what to build first, for whom, and why. This document records that decision. It is the narrowest point of the pyramid and the first document of Phase 2.

If any Phase 2 engineering decision contradicts this document, the contradiction must be resolved here before the code is written, not after.

---

## Sign-off

Wedge confirmed by: Silvester Ndaigiri and James Kabingu, Vektasafe Date: June 2026

Until this field is signed, this document is a proposal, not a decision. Phase 2 engineering does not start until this is filled.

---

## The Wedge

One sentence: Poetry in Motion's Phase 2 MVP is an AI-assisted style quiz and curated micro-catalog connecting Nairobi women to verified local creators, with M-Pesa checkout and WhatsApp-native sharing.

Everything not in that sentence is explicitly deferred.

---

## What the Research Produced

Each layer of the pyramid contributed one constraint or decision to this wedge.

| Layer | Document | Contribution to MVP |
|-------|----------|---------------------|
| Foundation | 00-foundation/FOUNDATION.md | The problem is fit, representation, and accountability. The customer is underserved by existing platforms. |
| Global e-commerce history | 01-global/LANDSCAPE.md | Personalisation loops (quiz to profile to recommendation) are proven. Scope before unit economics kills companies. |
| Global e-commerce industry | 01-global/INDUSTRY-ECOMMERCE.md | Take rate of 10 to 18% is the sustainable range. Creator share of 40 to 50% requires spreadsheet proof. |
| Global fashion industry | 01-global/INDUSTRY-FASHION.md | Curation beats endless scroll. Returns are the unit economics killer. Circular needs operations, not UI. |
| Africa | 02-africa/AFRICA.md | Social commerce is the incumbent. M-Pesa and WhatsApp are not optional. |
| East Africa | 02-africa/EAST-AFRICA.md | EAC is the natural second market. Design the data model for multi-currency from the start. |
| Kenya | 02-africa/KENYA.md | Nairobi is the launch city. The customer is already buying via Instagram and M-Pesa. Paystack is the Phase 2 payment provider. |
| Entities | 03-market-intelligence/ENTITIES.md | ShopZetu is the closest peer. The wedge must be AI styling plus circular plus creator voting, not another fashion mall. Social sellers are the creator onboarding pool. |
| Open-source reference | 04-technical-research/OPEN-SOURCE-REFERENCE.md | Stay on custom Next.js short-term. Evaluate Medusa v2 in a one-week spike. Implement 8 core APIs, not 45. |
| Project structure | 04-technical-research/PROJECT-STRUCTURE.md | Layers 1 and 2 (identity and commerce core) must be real before Layers 3 through 5 are expanded. |
| Critical review | 05-critical-review/CRITICAL-REVIEW.md | P0 actions must be complete before any public user touches the product. |

---

## MVP Specification

### Customer

Nairobi woman, 25 to 40 years old. Buys fashion online occasionally. Frustrated by poor fit, limited local creator visibility, and the gap between what she sees on Instagram and what she can actually purchase with confidence.

### Job to Be Done

"Help me find three outfits I would actually wear for work and weekends, from creators I can trust, without having to scroll through a thousand options."

### Flow

1. Style quiz (persisted to database on submit).
2. Twelve curated SKUs from five verified local creators, matched to quiz profile.
3. Product detail with creator story and honest fit notes.
4. M-Pesa checkout via Paystack.
5. Delivery partner quoted at checkout (partner courier or creator-managed).
6. WhatsApp-shareable quiz result and order status.

### Creator Supply

Five to ten Nairobi-based creators who are currently selling via Instagram or WhatsApp. Onboarding offer: logistics, payments, and discovery infrastructure they currently lack. No creator is listed without a signed creator agreement covering design ownership, photo rights, and payout timing.

### Technical Scope (Phase 2)

Implement 8 core API routes with a real database (Postgres plus Prisma):

1. auth (login, signup with hashed passwords and HTTP-only cookies)
2. profile (quiz results persisted)
3. products (real SKUs from onboarded creators)
4. cart
5. order
6. creator list
7. collection vote
8. trade-in intent (intake form only; no logistics yet)

Freeze all other routes at mock. Do not expand the API surface until these 8 are production-hardened.

### What Is Explicitly Deferred

| Feature | Reason for deferral |
|---------|---------------------|
| Live sessions | Requires real-time infrastructure. Not MVP. |
| Subscriptions | Requires billing. Not MVP. |
| Trade-in logistics | Requires reverse logistics partner. Not MVP. |
| Global resale | Requires authentication of goods. Not MVP. |
| Verified sustainability metrics | Requires chain-of-custody data. Not MVP. |
| AR try-on | Cost and consent surface too large. Not Phase 2. |
| National marketplace scale | Requires logistics network. Not Phase 2. |
| EAC expansion | Kenya must reach PMF first. Not Phase 2. |
| 37 remaining API routes | Facade risk. Freeze until core 8 are real. |

---

## Honesty Requirements (P0 Before Any Public User)

These are not optional. They are preconditions for any public deployment.

1. DEMO_MODE environment flag: blocks real checkout in public deploys.
2. No CO2, water, or verified labels on any SKU without a sustainability_source_id in the database.
3. No AI confidence scores in the UI until they are calibrated against real outcomes.
4. StyleAI label removed from all UI strings, manifest.json, and metadata.
5. package.json name field set to poetry-in-motion.
6. ODPC registration completed before collecting any user data.
7. Creator agreement template signed by all onboarded creators before their products are listed.

---

## Success Criteria for Phase 2 MVP

Phase 2 is not complete until:

- [ ] 5 creators onboarded with signed agreements
- [ ] 12 or more real SKUs in the database
- [ ] Quiz persisted to database on submit
- [ ] M-Pesa checkout live via Paystack
- [ ] WhatsApp order status sharing functional
- [ ] ODPC registration complete
- [ ] DEMO_MODE flag implemented
- [ ] All P0 honesty requirements met
- [ ] Unit economics spreadsheet built: AOV, return rate, take rate, M-Pesa fee, shipping, creator share
- [ ] Return rate measured from first 50 orders

---

## What Phase 3 Requires from Phase 2

Phase 3 (real recommendations, verified sustainability, EAC expansion) cannot start until Phase 2 produces:

- Real quiz completion and return rate data (minimum 200 users)
- Real return rate data (minimum 50 orders)
- At least one creator drop completed end-to-end (draft, voting, production, available)
- Unit economics spreadsheet validated against actual transactions
- One logistics partner with a signed SLA

---

## Pending P0 Items

The following P0 items from CRITICAL-REVIEW.md and the Honesty Requirements are not yet resolved. They must be completed before any public user touches the product.

- [ ] ODPC registration completed (MVP Honesty Requirement 6)
- [ ] Creator agreement template signed by all onboarded creators (MVP Honesty Requirement 7)
- [ ] One‑page strategy document created (CRITICAL‑REVIEW 6.1)
- [ ] Link to CRITICAL‑REVIEW added to README (CRITICAL‑REVIEW 6.2)
- [ ] Founder sign‑off on MVP wedge (this document, sign‑off field above)
- [ ] Creator revenue share contradiction resolved (40‑50% vs 82‑90%)
- [ ] M‑Pesa checkout implementation (Paystack or Daraja API access)
- [ ] Primary research interviews (two interviews, write‑up in 02‑africa/PRIMARY‑RESEARCH.md)
- [ ] Technical infrastructure gates (database, auth, payments, creator payout rails)
- [ ] Legal and compliance gates (Kenya Data Protection Act compliance, pre‑owned authenticity policy, creator agreement draft, children’s data protection)
- [ ] Market validation gates (East Africa entity research, logistics partner, creator onboarding)
- [ ] Sign‑off checklist for Phase 2 start (all of the above)

## References

- 00-foundation/FOUNDATION.md
- 01-global/LANDSCAPE.md
- 01-global/INDUSTRY-ECOMMERCE.md
- 01-global/INDUSTRY-FASHION.md
- 02-africa/AFRICA.md
- 02-africa/EAST-AFRICA.md
- 02-africa/KENYA.md
- 03-market-intelligence/ENTITIES.md
- 04-technical-research/OPEN-SOURCE-REFERENCE.md
- 04-technical-research/PROJECT-STRUCTURE.md
- 05-critical-review/CRITICAL-REVIEW.md
