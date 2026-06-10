# Poetry in Motion: The Transaction

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Phase 1 foundation document
Depends on: 00-foundation/PERSONAS.md, 02-africa/KENYA.md, 03-market-intelligence/ENTITIES.md, 03-market-intelligence/UNIT-ECONOMICS.md
Informs: 06-mvp/MVP.md, 04-technical-research/PROJECT-STRUCTURE.md
Last updated: June 2026

---

## Purpose

This document walks through one complete transaction on Poetry in Motion from the moment Wanjiru feels the need to the moment she rates the product. At each step it names the infrastructure requirement that step creates.

This is the application of the founding methodology: the product determines the infrastructure. Every infrastructure decision in this research must trace back to a specific step in this sequence. Infrastructure that cannot be traced to a step in this document is out of scope for the MVP.

---

## The Transaction

### Step 1: The need

Wanjiru is getting ready for a Saturday evening out. She has ochre wide-leg trousers and a black top. The look is not finished. She does not know what is missing. She knows she will recognise it when she sees it.

She opens Poetry in Motion.

**Infrastructure requirement:** Mobile-first PWA or app. Fast load on Nairobi 4G. No desktop assumption.  
**Existing coverage:** [IMPLEMENTED] app/layout.tsx, mobile components, public/sw.js  
**Gap:** Performance on low-bandwidth has not been tested against real Nairobi connectivity.

---

### Step 2: The profile

She does not search. She does not scroll a generic grid. Her style quiz profile from two weeks ago is already persisted. The app reads it: deep skin tone, hourglass, earth tones and jewel tones, social occasions, budget KSh 3,000 to 8,000.

The feed surfaces a curated selection matched to her profile and tonight's occasion.

**Infrastructure requirement:** Quiz results persisted to a real database on submission. Profile readable by the recommendations engine on every session.  
**Existing coverage:** [IMPLEMENTED] mock only. app/api/style-profile/route.ts reads from in-memory mock.  
**Gap:** No database. Quiz results are lost on reload. This is P0 for Phase 2. See 06-mvp/MVP.md API route 2.

---

### Step 3: The discovery

She sees a crochet co-ord set from Zawadi, a Nairobi-based designer. The product photo is clean: properly lit, true colour, texture visible, scale clear. She can see Zawadi's name, neighbourhood, and materials. The price is KSh 4,500.

She also sees a pre-owned silk shirt in burnt orange listed by another user through the trade-in flow. Condition verified. KSh 1,200. Mali Safi.

**Infrastructure requirement — photography:** Product photo must be trustworthy on a 6-inch screen. Zawadi cannot be expected to produce this unaided. A photography standard must be defined and enforced at creator onboarding. This is a supply-side infrastructure requirement, not a technical one.  
**Existing coverage:** No photography standard document exists in Phase 1 research.  
**Gap:** PHOTOGRAPHY-STANDARD.md is required. It belongs in 04-technical-research/ and must be written before creator onboarding begins. It is a Phase 2 gate item.

**Infrastructure requirement — pre-owned condition:** The pre-owned listing must carry a verified condition label that means something. Someone must inspect or vouch for the item before it is listed as Mali Safi.  
**Existing coverage:** [IMPLEMENTED] mock. app/api/pre-owned/route.ts and lib/types.ts PreOwnedListing exist.  
**Gap:** No condition verification process exists. The circular flow is UI without operations. ThredUp lesson from ENTITIES.md applies: do not open circular UI without intake and grading process. Deferred to Phase 2 per MVP.md.

---

### Step 4: The decision

She taps the co-ord set. One screen. Her size is in stock. Her colour is available. Fit notes from Zawadi read: runs true to size, stretches slightly at the waist.

She taps buy.

**Infrastructure requirement — product data:** Size, colour, stock level, and fit notes must be real fields from a real database, not mock. A product with no stock state cannot be sold.  
**Existing coverage:** [IMPLEMENTED] mock. lib/types.ts Product type has sizes, colors, inStock.  
**Gap:** No database. Stock is fictional. Real inventory requires Phase 2 database and creator product upload flow.

**Infrastructure requirement — fit notes:** The current Product type has no fit notes field. This is a [HYPOTHESIS] feature referenced in CRITICAL-REVIEW.md Part 6.3. It reduces returns. It must be added to lib/types.ts in Phase 2.

---

### Step 5: Payment

M-Pesa STK push hits her phone. She confirms. The transaction completes in under 40 seconds.

**Infrastructure requirement:** M-Pesa STK push via Paystack or Daraja API. This is not optional. The transaction does not exist without it. Card checkout is a secondary path, not the primary.  
**Existing coverage:** [IMPLEMENTED] mock only. app/api/orders/route.ts creates an order object but processes no real payment.  
**Gap:** M-Pesa integration is P0 for Phase 2. Paystack recommended in KENYA.md. Daraja direct at volume. This is the single most critical Phase 2 technical gate.

**Infrastructure requirement — split payout:** When Wanjiru pays, Zawadi's share (82 to 90% of sale price) must be held and scheduled for monthly payout. The platform retains its 10 to 18% commission. Paystack Split or Flutterwave subaccounts are the mechanism.  
**Existing coverage:** None. Creator payout rails do not exist in Phase 1.  
**Gap:** Creator payout is a Phase 2 gate item. It requires KYC, a payout schedule, and a tax handling decision. See UNIT-ECONOMICS.md creator economics and MVP.md P0 items.

---

### Step 6: Fulfilment

Zawadi receives a notification. She packages the order. Poetry in Motion's logistics partner schedules a pickup from her the next morning. Wanjiru receives a tracking update. The order arrives.

**Infrastructure requirement — creator notification:** Zawadi must be notified immediately on sale. WhatsApp or SMS is the reliable channel, not email.  
**Existing coverage:** [IMPLEMENTED] mock. app/api/community/notifications/route.ts exists but is in-memory.  
**Gap:** Real notification requires a real database and a WhatsApp Business API or SMS gateway integration. Phase 2 item.

**Infrastructure requirement — logistics partner:** A named courier must be contracted before a single real order is placed. Creator-managed delivery is the MVP default for Nairobi but is not scalable. At minimum one courier with a quoted rate for Nairobi urban delivery must be in place before public launch.  
**Existing coverage:** None. No logistics partner is named or contracted in Phase 1.  
**Gap:** This is a Phase 2 market validation gate per CRITICAL-REVIEW.md Part 11.5. Three courier quotes are required. Sendy failure from KENYA.md is the cautionary reference. Do not build logistics dependency before product-market fit.

---

### Step 7: Rating and feedback loop

Wanjiru rates the piece. Four stars. Fit was accurate. Delivery was one day. That rating feeds Zawadi's creator profile score and refines Wanjiru's future recommendations. The next time Wanjiru opens the app, the AI knows her slightly better.

**Infrastructure requirement — ratings persistence:** Ratings must be stored in a real database and read by the recommendations engine. A rating stored nowhere improves nothing.  
**Existing coverage:** [IMPLEMENTED] mock. app/api/community/reviews/route.ts exists.  
**Gap:** No database. Ratings loop is fictional until Phase 2 database exists.

**Infrastructure requirement — recommendations improvement:** The recommendations engine must consume real ratings data over time. This is the personalisation flywheel described in LANDSCAPE.md Part 1.5 and the Stitch Fix lesson in ENTITIES.md. It does not work on mock data.  
**Existing coverage:** [IMPLEMENTED] mock. Rule-based-profile-match-v1 per CRITICAL-REVIEW.md Part 10.  
**Gap:** Real ML recommendations require real data from real transactions. Phase 3 item. Phase 2 uses rule-based matching explicitly labelled as such.

---

## Infrastructure Requirements Summary

| Step | Requirement | Phase | Document reference | Status |
|------|-------------|-------|--------------------|--------|
| 1. Open app | Mobile PWA, 4G performance | 2 | PROJECT-STRUCTURE.md Layer 1 | [IMPLEMENTED] not tested |
| 2. Profile read | Quiz persisted to database | 2 | MVP.md API route 2 | [HYPOTHESIS] |
| 3. Discovery | Photography standard for creators | 2 | PHOTOGRAPHY-STANDARD.md (pending) | Missing document |
| 3. Discovery | Pre-owned condition verification process | 2 | MVP.md deferred list | [HYPOTHESIS] |
| 4. Decision | Real product database with stock | 2 | MVP.md API route 3 | [HYPOTHESIS] |
| 4. Decision | Fit notes field on Product type | 2 | CRITICAL-REVIEW.md 6.3 | [HYPOTHESIS] |
| 5. Payment | M-Pesa STK push via Paystack | 2 | KENYA.md payments, MVP.md P0 | [HYPOTHESIS] |
| 5. Payment | Creator split payout rails | 2 | UNIT-ECONOMICS.md, MVP.md P0 | Missing |
| 6. Fulfilment | WhatsApp or SMS creator notification | 2 | MVP.md API route 7 | [HYPOTHESIS] |
| 6. Fulfilment | Named logistics partner, Nairobi courier | 2 | CRITICAL-REVIEW.md 11.5 | Missing |
| 7. Rating | Ratings database persistence | 2 | PROJECT-STRUCTURE.md Layer 4 | [HYPOTHESIS] |
| 7. Rating | Recommendations learning from real data | 3 | PROJECT-STRUCTURE.md Layer 3 | [RESEARCH DIRECTION] |

---

## What This Document Adds to the Research

The infrastructure items in KENYA.md, ENTITIES.md, and UNIT-ECONOMICS.md were derived from market research. This document derives the same infrastructure from the product sequence. Where the two approaches agree, confidence is higher. Where they differ, the product sequence takes precedence for MVP scoping.

One item this document surfaces that no existing document covers: PHOTOGRAPHY-STANDARD.md. Zawadi's product photo is load-bearing for Wanjiru's trust. Without a defined and enforced photography standard at creator onboarding, the discovery step fails regardless of how good the AI matching is. This document is a Phase 2 gate item and must be added to 04-technical-research/ before creator onboarding begins.

---

## References

- 00-foundation/PERSONAS.md: Wanjiru and Zawadi in full
- 00-foundation/FOUNDATION.md: core pillars
- 02-africa/KENYA.md: M-Pesa, logistics, creator landscape
- 03-market-intelligence/ENTITIES.md: Paystack, logistics cautionary (Sendy), ThredUp circular lesson
- 03-market-intelligence/UNIT-ECONOMICS.md: creator share, payment fees, return rate risk
- 04-technical-research/PROJECT-STRUCTURE.md: five-layer architecture and notation
- 05-critical-review/CRITICAL-REVIEW.md: P0 items, Phase 2 gates
- 06-mvp/MVP.md: Phase 2 API routes, deferred list, success criteria
