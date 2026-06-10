# Poetry in Motion: Personas

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Phase 1 foundation document
Depends on: 00-foundation/FOUNDATION.md, 02-africa/KENYA.md, 03-market-intelligence/ENTITIES.md
Informs: 06-mvp/MVP.md, 00-foundation/TRANSACTION.md
Last updated: June 2026

---

## Purpose

This document names the two people Poetry in Motion exists to serve. Every assumption in KENYA.md, MVP.md, and ENTITIES.md must be challengeable against one of these two people. If a product decision cannot be traced to Wanjiru or Zawadi, it is out of scope.

These are archetypes derived from desk research and the Kenya creator and consumer landscape documented in 02-africa/KENYA.md and 03-market-intelligence/ENTITIES.md. They are [ASSUMED] until PRIMARY-RESEARCH.md is complete. Primary research interviews must challenge and correct the assumptions below.

---

## Persona 1: The Customer

**Name:** Wanjiru  
**Age:** 27  
**Location:** Nairobi. Works in Upperhill or Westlands. Finance, tech, or NGO sector.  
**Income:** Earns enough for discretionary spend. Not enough to waste it.  
**Device:** Phone is her primary computer. M-Pesa is her default payment method.  
**Trust signal:** She trusts something when someone she follows has vouched for it.

### Her situation

Wanjiru knows her taste. She cannot find it reliably online.

She has tried Jumia. Quality is unpredictable on arrival. She has tried global brands. Nothing fits her hips right. She has bought from a seller at Maasai Market twice and has no way to return to the same seller. She scrolls Instagram and sees Kenyan creators doing extraordinary work but cannot find where to actually buy it, in her size, delivered reliably, with a return process if something is wrong.

She wants to look intentional at work. Distinctive at social events. She is tired of wearing the same rotation because she cannot find new pieces she trusts.

She also has clothes she no longer wears. She does not know how to move them responsibly without reverting to informal WhatsApp groups where transactions go cold.

### What she needs from Poetry in Motion

A curated feed matched to her body, skin tone, colour preferences, and occasion — not a generic catalog. Clean product photography she can trust on a 6-inch screen. A creator she can identify by name and location. M-Pesa checkout in under a minute. Reliable delivery to Nairobi. A simple trade-in path for what she no longer wears.

She does not need infinite choice. She needs three things she would actually wear.

### Assumptions to validate in PRIMARY-RESEARCH.md

| Assumption | Source | Risk if wrong |
|------------|--------|---------------|
| She pays by M-Pesa, not card | KENYA.md payments section | Payment flow changes entirely |
| She discovers via Instagram, not search | KENYA.md informal sellers section | Acquisition channel changes |
| Fit and returns are her primary frustration | MVP.md job-to-be-done | Core product premise changes |
| She has discretionary spend of KSh 3,000 to 8,000 per purchase | MVP.md AOV assumption | Unit economics model changes |
| She trusts creator identity and location as a quality signal | [ASSUMED] | Creator onboarding priority changes |

---

## Persona 2: The Creator

**Name:** Zawadi  
**Location:** Nairobi. May also be based in Mombasa, Kisumu, or another Kenyan city.  
**What she makes:** Crochet co-ords, kitenge ready-to-wear, boutique-curated pieces, or second-hand curation from Gikomba. The specific category varies. The situation is consistent.  
**Sales channel:** Instagram DMs and WhatsApp. Occasionally physical market.  
**Followers:** Hundreds to low thousands. Engaged but not scaled.

### Her situation

Zawadi makes or curates beautiful things. She sells through Instagram DMs and WhatsApp broadcasts. She has no storefront, no analytics, no consistent product photography, and no reliable way to reach buyers outside her existing network.

She loses sales every week because a DM conversation goes cold before M-Pesa is sent. She has no idea which of her pieces performs best because she has no data. Her photography is inconsistent because she shoots on her phone in available light when she has time. She has occasionally sold through a cousin's network or a WhatsApp group but has no infrastructure to make that repeatable.

She does not need a loan. She does not need training. She needs a platform that photographs her work to a standard buyers trust, matches it to the right buyer through AI, handles payment and delivery, and pays her reliably on a published schedule.

The creator types Poetry in Motion serves share Zawadi's situation:

| Creator type | Product | Current channel |
|--------------|---------|-----------------|
| Traditional and cultural makers | Kitenge tailors, kikoy textile designers, Maasai-influenced ready-to-wear | Instagram, physical markets |
| Crochet designers | Bags, tops, co-ords | Instagram DMs, WhatsApp |
| Boutique owners | Curated new pieces, small physical shop | Walk-in, Instagram, word of mouth |
| Mitumba curators | Second-hand, Gikomba-sourced | WhatsApp groups, Jiji listings |
| Individual resellers | Pre-owned pieces from their own wardrobe | WhatsApp, informal networks |

### What she needs from Poetry in Motion

A storefront she does not have to build. A photography standard she can meet without a studio. A buyer pool she could not reach alone. M-Pesa payout on a schedule she can plan around. A creator agreement that is clear on IP, photo rights, and revenue share before she lists a single piece.

She needs to earn enough per month from the platform to consider it a real channel, not a side experiment. The minimum viable GMV that makes this worth her time is [UNKNOWN] and must be established in creator interviews before Phase 2.

### Assumptions to validate in PRIMARY-RESEARCH.md

| Assumption | Source | Risk if wrong |
|------------|--------|---------------|
| She sells via Instagram DMs and WhatsApp today | KENYA.md informal sellers, ENTITIES.md Group 8 | Onboarding pitch changes entirely |
| Photography quality is a barrier to her moving online | [ASSUMED] | Photography standard requirement changes |
| She will accept 82 to 90% of sale price as revenue share | UNIT-ECONOMICS.md creator economics | Creator agreement and take rate change |
| She can fulfil Nairobi orders within 24 hours from her location | [ASSUMED] | Logistics model changes |
| She has inventory ready to list within 2 weeks of onboarding | [ASSUMED] | MVP supply timeline changes |

---

## How These Two People Connect

Wanjiru opens Poetry in Motion. The AI matches her profile to Zawadi's crochet co-ord set. Wanjiru buys. Zawadi fulfils. The platform handles payment, logistics coordination, and payout. Neither had to find the other. Neither had to trust a stranger alone. The platform is the trust layer between them.

That connection is the product. Everything else is infrastructure in service of it.

---

## What Happens When PRIMARY-RESEARCH.md Is Complete

Each assumption table above must be revisited row by row. Assumptions confirmed by interview are marked [CONFIRMED]. Assumptions contradicted are updated and the impact on MVP.md and TRANSACTION.md is documented explicitly.

Until PRIMARY-RESEARCH.md is complete, these personas are [ASSUMED] archetypes, not validated profiles.

---

## References

- 00-foundation/FOUNDATION.md: core problem statement
- 02-africa/KENYA.md: informal seller archetypes, payment and logistics context
- 03-market-intelligence/ENTITIES.md: Group 8 entity-driven MVP wedge
- 06-mvp/MVP.md: customer and creator supply definitions
- 06-mvp/PRIMARY-RESEARCH.md: interview write-ups (pending)
- 03-market-intelligence/UNIT-ECONOMICS.md: creator economics assumptions
