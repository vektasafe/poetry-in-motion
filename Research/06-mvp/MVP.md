# Poetry in Motion: MVP Definition

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Phase 1 apex document. Defines the Phase 2 engineering starting point.
Cross-reference: All Phase 1 documents. This document is the output of the pyramid.
Last updated: June 2026

---

## Purpose

Every layer of the Phase 1 research pyramid exists to justify one decision: what to build first, for whom, and why. This document records that decision. It is the narrowest point of the pyramid and the first document of Phase 2.

If any Phase 2 engineering decision contradicts this document, the contradiction must be resolved here before the code is written, not after.

---

## Sign-off

Wedge confirmed by: Silvester Ndaigiri and James Kabingu, Vektasafe
Date: June 2026

Until this field is signed, this document is a proposal, not a decision. Phase 2 engineering does not start until this is filled.

---

## The Wedge

One sentence: Poetry in Motion's Phase 2 MVP is an AI-assisted style quiz and curated micro-catalog connecting Nairobi women to verified local creators and vetted pre-owned pieces, with M-Pesa checkout and WhatsApp-native sharing.

Everything not in that sentence is explicitly deferred.

---

## What the Research Produced

Each layer of the pyramid contributed one constraint or decision to this wedge.

| Layer | Document | Contribution to MVP |
|-------|----------|---------------------|
| Foundation | 00-foundation/FOUNDATION.md | The problem is fit, representation, and accountability. The customer is underserved by existing platforms. Blue Ocean and Last Mover position confirmed. |
| Personas | 00-foundation/PERSONAS.md | Wanjiru is the customer. Zawadi is the creator. All MVP decisions trace to one of these two people. |
| Transaction | 00-foundation/TRANSACTION.md | The product determines the infrastructure. 7-step exchange maps all Phase 2 gates. |
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

Wanjiru. See 00-foundation/PERSONAS.md for full profile. In brief: Nairobi professional woman, 27, phone-first, M-Pesa default, knows her taste, cannot find it reliably. Frustrated by poor fit, limited local creator visibility, and the gap between what she sees on Instagram and what she can actually purchase with confidence.

### Creator

Zawadi. See 00-foundation/PERSONAS.md for full profile. In brief: Nairobi-based maker or curator selling via Instagram DMs and WhatsApp. Has product, has story, has no reliable infrastructure to reach Wanjiru.

### Job to Be Done

Wanjiru: "Help me find three pieces I would actually wear, from creators I can trust, without scrolling through a thousand options."

Zawadi: "Give me a storefront, handle my payments and delivery, and pay me reliably so this is worth my time."

### Flow

See 00-foundation/TRANSACTION.md for the complete 7-step exchange. Summary:

1. Style quiz persisted to database on submit
2. Curated feed of new and pre-owned pieces matched to quiz profile
3. Product detail with creator story, honest fit notes, and verified condition for pre-owned
4. M-Pesa checkout via Paystack
5. Delivery partner quoted at checkout (partner courier or creator-managed)
6. WhatsApp-shareable quiz result and order status
7. Rating feeds creator profile and recommendation refinement

### The Two Product Types

**New pieces** — listed by verified creators (Zawadi). Photographed to standard. Creator story visible. Fit notes required.

**Pre-owned pieces** — listed by platform users trading in their own clothing. Condition verified before listing. Mali Safi label applied only after verification. Intake and grading process required before circular UI is opened to public.

### Creator Supply

Five to ten Nairobi-based creators currently selling via Instagram or WhatsApp. Onboarding offer: logistics, payments, and discovery infrastructure they currently lack. No creator is listed without a signed creator agreement covering design ownership, photo rights, and payout timing.

Photography standard must be defined and distributed to all creators before onboarding begins. See 04-technical-research/PHOTOGRAPHY-STANDARD.md (Phase 2 gate item).

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
| Trade-in logistics | Requires reverse logistics partner. Not MVP. |
| Live sessions | Requires real-time infrastructure. Not MVP. |
| Subscriptions | Requires billing infrastructure. Not MVP. |
| Global resale | Requires authentication of goods. Not MVP. |
| Verified sustainability metrics | Requires chain-of-custody data. Not MVP. |
| AR try-on | Cost and consent surface too large. Not Phase 2. |
| National marketplace scale | Requires logistics network. Not Phase 2. |
| EAC expansion | Kenya must reach PMF first. Not Phase 2. |
| 37 remaining API routes | Facade risk. Freeze until core 8 are real. |

---

## Honesty Requirements (P0 Before Any Public User)

These are not optional. They are preconditions for any public deployment.

1. DEMO_MODE environment flag: blocks real checkout in public deploys until M-Pesa is live.
2. No CO2, water, or verified labels on any SKU without a sustainability_source_id in the database.
3. No AI confidence scores in the UI until they are calibrated against real outcomes.
4. StyleAI label removed from all UI strings, manifest.json, and metadata. Brand is Poetry in Motion.
5. package.json name field set to poetry-in-motion.
6. ODPC registration completed before collecting any user data.
7. Creator agreement template signed by all onboarded creators before their products are listed.
8. Mali Safi label applied only to pre-owned items that have passed condition verification. No label without a verified_condition field in the database.

---

## Success Criteria for Phase 2 MVP

Phase 2 is not complete until:

- [ ] 5 creators onboarded with signed agreements
- [ ] 12 or more real SKUs in the database (new and pre-owned combined)
- [ ] Quiz persisted to database on submit
- [ ] M-Pesa checkout live via Paystack
- [ ] WhatsApp order status sharing functional
- [ ] Pre-owned intake and condition verification process operational
- [ ] Photography standard document written and distributed to creators
- [ ] ODPC registration complete
- [ ] DEMO_MODE flag implemented
- [ ] All P0 honesty requirements met
- [ ] Unit economics spreadsheet built: AOV, return rate, take rate, M-Pesa fee, shipping, creator share
- [ ] Creator revenue share contradiction resolved: 40 to 50% product copy versus 82 to 90% UNIT-ECONOMICS.md. One number, spreadsheet-proven.
- [ ] Return rate measured from first 50 orders

---

## What Phase 3 Requires from Phase 2

Phase 3 (real recommendations, verified sustainability, EAC expansion) cannot start until Phase 2 produces:

- Real quiz completion and return rate data (minimum 200 users)
- Real return rate data (minimum 50 orders)
- At least one creator drop completed end-to-end (draft, voting, production, available)
- Unit economics spreadsheet validated against actual transactions
- One logistics partner with a signed SLA
- Primary research interviews completed (00-foundation/PERSONAS.md assumptions validated)

---

## Pending P0 Items

The following P0 items from CRITICAL-REVIEW.md and the Honesty Requirements are not yet resolved. They must be completed before any public user touches the product.

- [ ] ODPC registration completed (MVP Honesty Requirement 6)
- [ ] Creator agreement template signed by all onboarded creators (MVP Honesty Requirement 7)
- [ ] Photography standard document written (TRANSACTION.md Step 3 gap)
- [ ] Pre-owned condition verification process defined (TRANSACTION.md Step 3 gap)
- [ ] Creator payout rails defined (TRANSACTION.md Step 5 gap)
- [ ] Logistics partner contracted with Nairobi courier quote (TRANSACTION.md Step 6 gap)
- [ ] One-page strategy document created (CRITICAL-REVIEW 6.1)
- [ ] Link to CRITICAL-REVIEW added to README (CRITICAL-REVIEW 6.2)
- [ ] Founder sign-off on MVP wedge (this document, sign-off field above)
- [ ] Creator revenue share contradiction resolved (40 to 50% vs 82 to 90%)
- [ ] M-Pesa checkout implementation (Paystack or Daraja API access)
- [ ] Primary research interviews (two interviews, write-up in 02-africa/PRIMARY-RESEARCH.md)
- [ ] Technical infrastructure gates (database, auth, payments, creator payout rails)
- [ ] Legal and compliance gates (Kenya Data Protection Act compliance, pre-owned authenticity policy, creator agreement draft, children's data protection)
- [ ] Market validation gates (East Africa entity research, logistics partner, creator onboarding)
- [ ] Sign-off checklist for Phase 2 start (all of the above)

---

## References

- 00-foundation/FOUNDATION.md
- 00-foundation/DATA-ETHICS.md
- 00-foundation/PERSONAS.md
- 00-foundation/TRANSACTION.md
- 01-global/LANDSCAPE.md
- 01-global/INDUSTRY-ECOMMERCE.md
- 01-global/INDUSTRY-FASHION.md
- 02-africa/AFRICA.md
- 02-africa/EAST-AFRICA.md
- 02-africa/KENYA.md
- 03-market-intelligence/ENTITIES.md
- 03-market-intelligence/UNIT-ECONOMICS.md
- 04-technical-research/OPEN-SOURCE-REFERENCE.md
- 04-technical-research/PROJECT-STRUCTURE.md
- 05-critical-review/CRITICAL-REVIEW.md
