# Poetry in Motion: Critical Review

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Living document. Challenges Phase 1 research and prototype claims.
Cross-reference: 00-foundation/FOUNDATION.md, 01-global/LANDSCAPE.md, 04-technical-research/PROJECT-STRUCTURE.md
Last updated: June 2026

---

## Purpose

Phase 1 research builds a convincing origin story: history, ethics, architecture. That narrative is useful but not sufficient. This document contradicts where the research overclaims, names what is good and what fails honestly, lists weaknesses and hard limitations, and gives recommended fixes with priority.

If foundation documents and this review disagree, this review takes precedence until evidence closes the gap.

---

## Part 1: Internal Contradictions in the Research

These are tensions within Phase 1 documents that are not yet resolved.

| Claim A (research) | Claim B (same research or code) | Why it contradicts |
|--------------------|----------------------------------|-------------------|
| "Not a race-to-the-bottom marketplace" | Inherits Amazon and eBay reliable checkout, catalog, and cart as core Layer 2 | Industrial commerce is the gravity well. Without discipline, ethics become marketing on top of commodity retail. |
| "Intelligence over infinite scroll" | Shop, recommendations, and 19 pages of browse UX | The prototype still looks like discovery through catalog, not through a narrow styling outcome. |
| "Reject bolt-on sustainability" | Product type includes sustainability blocks; UI can show metrics with no data pipeline | Bolt-on risk is already present in mocks. The research pretends it is future-only. |
| "Creators as partners" (40 to 50% share in copy) | No payout rails, KYC, tax, or dispute flow in structure document | Partnership language without payment enforcement is the same extractive pattern Etsy sellers criticise. |
| "Representation is a product requirement" | Quiz uses Western fit taxonomy (pear, hourglass, inverted triangle) | Those categories are not neutral. They import a global sizing ideology that LANDSCAPE never critiques. |
| "Not trying to be Stitch Fix, Shein, or Amazon" | Positioning explicitly combines Stitch Fix, Etsy, ThredUp, and African mobile commerce | Four proven business models at once is the Boo.com failure mode: scope before unit economics. |
| "Prototype honesty" (pillar 5) | Legacy brand StyleAI still in UI; "verified" creator flags present | Honesty is partial. Users would still see false certainty. Solved. See Part 10. |
| LANDSCAPE "refuse opaque algorithms" | AI routes return hard-coded JSON with high confidence: 0.92 | Mock certainty trains the team to ship false precision, which is worse than no AI. |
| "East Africa first" in implications | No COD, M-Pesa, SMS, or logistics partners in code or Phase 1 exit criteria | Regional thesis is research text only until Phase 2 ENTITIES and payments exist. |
| Phase 1 exit: "internally consistent" | This document shows inconsistency by design | Consistency was narrative, not validated against market or law. |

Verdict: Phase 1 is a strong directional essay, not a validated strategy. Treat implications tables as hypotheses, not decisions.

---

## Part 2: What to Keep

| Strength | Why it is real | Protect it by |
|----------|----------------|---------------|
| Historical grounding | LANDSCAPE explains why marketplaces won and fast fashion hurt. Avoids reinventing naively. | Keep updating LANDSCAPE when strategy shifts. Cite dates. |
| Explicit reject list | Part 3.2 names patterns to avoid: greenwashing, opaque algorithms, platform rent. | Turn each reject into a testable policy. See Part 6. |
| Layered architecture document | PROJECT-STRUCTURE maps pillars to routes and mocks. | Use tags [IMPLEMENTED] and [HYPOTHESIS] on every new feature. |
| Creator collection lifecycle | draft, voting, production, available is a distinct demand signal. | Ship one creator drop end-to-end before more APIs. |
| Circular module in the model | Trade-in and pre-owned types exist early. | Do not show CO2 or water until source and methodology are documented. |
| Quiz to profile to recommend path | Matches proven styling funnel (Stitch Fix lesson). | Persist quiz results. Measure completion and return rate. |
| Phase boundaries (Ganji-style) | Stops production sustainability claims before supply data exists. | Enforce hard gate in README and PR checklist. |
| Research separated from app code | Reduces v0 throwaway risk. | All strategy changes go through Research/ first. |
| Africa commerce called out | M-Pesa, COD, WhatsApp selling acknowledged. | Phase 2 ENTITIES must name actual partners, not "integrate M-Pesa" in abstract. |

---

## Part 3: What Fails or Misleads

| Problem | Evidence | Impact if ignored |
|---------|----------|-------------------|
| Scope inflation | 5 layers, 45 APIs, 19 pages, 4 strategic lineages | Burnout, Boo.com-style collapse, nothing works end-to-end |
| Ethics without enforcement | Body type and skin tone collected; no consent ledger, retention policy, or audit | Regulatory and reputational risk under Kenya Data Protection Act and for EU visitors. Partially mitigated. See Part 10. |
| Fictional impact data | mock-data sustainability numbers; circular page shows CO2 and water | Greenwashing if shipped publicly. Illegal in several jurisdictions as misleading consumer information. Solved. See Part 10. |
| False AI | Image analysis returns fixed "minimalist, 0.92 confidence" | Destroys trust when users test it once. Solved. See Part 10. |
| Security theatre | Base64 token auth | Any demo on the internet is a liability. Partially mitigated. See Part 10. |
| No unit economics | No CAC, margin, return rate, take rate, or logistics cost | Cannot know if 40 to 50% creator share is solvent. Partially mitigated. See Part 10. |
| Personalisation moat assumed | Stitch Fix struggled at times; Shein wins on price and speed | Quiz alone is not a moat without inventory and fit outcomes. Partially mitigated. See Part 10. |
| Movement language | Hero copy versus transactional shop | Confuses team priorities: brand NGO versus retailer. Solved. See Part 10. |
| v0 heritage | Generic stack, my-v0-project package name | Signals demo, undermines Poetry in Motion brand. Solved. See Part 10. |

---

## Part 4: Weaknesses and Limitations

### 4.1 Research Process Limitations

| Limitation | Detail |
|------------|--------|
| No primary research | No interviews with designers, thrifters, or Nairobi shoppers in Phase 1 |
| No quantitative market sizing | TAM, SAM, and SOM are absent |
| Literature cited as categories | McKinsey and Ellen MacArthur listed but not applied to numbers |
| Single author bias | One worldview; no red-team until this document |

### 4.2 Market and Business Limitations

| Limitation | Detail |
|------------|--------|
| Logistics | Fashion e-commerce in Kenya: returns, last mile, and COD fraud are harder than payments |
| Inventory | Creator voting without manufacturing partners is theatre |
| Trust | Pre-owned needs authentication. Luxury resale spent years on it. |
| Payment margin | M-Pesa fees plus refunds eat thin fashion margins |
| Incumbent habit | WhatsApp catalog plus M-Pesa P2P is good enough for many buyers |

### 4.3 Technical Limitations

| Limitation | Detail |
|------------|--------|
| Mock-only backend | Cannot learn from real failure modes such as stockouts and chargebacks |
| No fit science | Body type quiz does not equal measurements. Return rates will stay high. |
| No ML ops | Recommendations are placeholders. Cold start is unsolved. |
| PWA and offline | Basic service worker. Not an offline-first Africa connectivity strategy. |
| 45 routes | Maintenance cost with 3 products in mock data |

### 4.4 Ethical and Legal Limitations

| Limitation | Detail |
|------------|--------|
| Sensitive attributes | Skin tone and body type can reinforce exclusion if models are wrong |
| Sustainability claims | Without chain of custody, metrics are opinion |
| Creator labour | Revenue share copy does not guarantee minimum wage or IP ownership |
| Children's data | Fashion apps can attract minors. No age gate in research. |

---

## Part 5: Research versus Prototype Gap Table

| Research promise | Prototype reality | Gap severity |
|------------------|-------------------|--------------| 
| Poetry in Motion brand | UI: StyleAI | High. User-facing. |
| Verified sustainability | Static numbers | Critical. Do not publish. |
| AI styling | Mock JSON | Critical. Label "demo" in UI. |
| Creator economy | 2 mock creators, no payouts | High |
| Circular fashion | UI only | High |
| M-Pesa and Africa-first | Card-style commerce assumptions | High |
| Community and live | Routes exist, no streaming | Medium |
| 45 API platform | One JSON file of data | High. Facade risk. |

---

## Part 6: Recommendations

Priorities: P0 (before any public repository or users), P1 (Phase 2 MVP), P2 (scale), P3 (later).

### 6.1 Strategy

| Problem | Recommendation | Priority |
|---------|----------------|----------|
| Four business models at once | Choose one lead wedge for 12 months. Example: AI style quiz plus curated micro-catalog from 10 Kenyan creators. Park resale, live, and subscriptions. | P0 |
| Movement versus retailer confusion | Write a one-page strategy. Primary revenue equals commission on GMV, subscription styling, or B2B creator SaaS. | P0 |
| No unit economics | Build a spreadsheet model: AOV, return percentage, take rate, M-Pesa fee, shipping, creator share. Kill features that fail margin. | P1 |

### 6.2 Research

| Problem | Recommendation | Priority |
|---------|----------------|----------|
| Africa under-researched | 02-africa/ layer now exists. Add AFRICA-RETAIL.md in Phase 2: COD fraud, courier partners, Fashionomics Africa, KEBS and textile rules. | P1 |
| Implications untested | For each LANDSCAPE 3.2 reject, add an acceptance criterion. Example: no SKU without sustainability source ID. | P1 |
| This review orphaned | Link CRITICAL-REVIEW from README. Revisit quarterly. | P0 |

### 6.3 Product

| Problem | Recommendation | Priority |
|---------|----------------|----------|
| StyleAI branding | Global rename to Poetry in Motion in app/, manifest.json, and metadata | P0 |
| Fake metrics | Remove or grey out CO2 and water until methodology document exists. Show "impact data pending". | P0 |
| Fake AI confidence | Demo mode banner plus randomness disclaimer. Never show 0.92 in production. | P0 |
| Western body taxonomy | Research regional sizing (UK and KE designers, inclusive mannequins). Add "fit notes" free text. Reduce reliance on pear and hourglass. | P1 |
| Quiz not persisted | Save profile to DB on submit. Single source for recommendations. | P1 |

### 6.4 Technical

| Problem | Recommendation | Priority |
|---------|----------------|----------|
| 45 mock APIs | Freeze API surface. Implement 8 core routes with Postgres: auth, profile, products, cart, order, creator list, collection vote, trade-in intent. | P1 |
| Base64 auth | Supabase Auth or Auth.js plus hashed passwords plus HTTP-only cookies | P0 if public |
| No payments | M-Pesa STK Push (Daraja) or Paystack for Kenya pilot, before subscriptions | P1 |
| No database | Postgres plus Prisma. Migrate lib/types.ts to schema. | P1 |
| Package name | Rename package.json to poetry-in-motion | P0 |

### 6.5 Ethics and Legal

| Problem | Recommendation | Priority |
|---------|----------------|----------|
| Sustainability claims | Partner with one traceability standard (example: batch-level fibre certification) or remove claims | P1 |
| Creator IP | Standard creator agreement template: who owns designs, photo rights, payout timing | P1 |
| Public demo risk | Environment flag DEMO_MODE=true. Block checkout in public deploys. | P0 |

### 6.6 What Not to Do

| Temptation | Why to skip it now |
|------------|-------------------|
| Launch public vektasafe/poetry-in-motion with current mocks | Greenwashing and security liability |
| Add more v0 features (AR try-on, crypto, NFT drops) | Deepens facade |
| Train custom LLM on body photos | Cost, consent, and bias surface too large for Phase 2 |
| Compete with Shein on SKU count | Wrong game |
| Promise "verified" without auditors | Same path as H&M greenwashing lawsuits |

---

## Part 7: Revised Phase 1 Exit Criteria

Phase 1 is not complete until:

- [x] History and structure written
- [x] Critical review written (this document)
- [x] ENTITIES.md baseline complete
- [x] DATA-ETHICS.md draft in place
- [x] Geographic narrowing documented: Africa, East Africa, Kenya
- [x] Wedge chosen: one sentence plus what is explicitly deferred
- [ ] ENTITIES extensions: interviews, courier quotes, TikTok Shop primary fees (Phase 2)
- [x] Public-facing demo rules: DEMO_MODE, no fake metrics

Phase 2 engineering starts after P0 items above are complete, not after more research pages are written.

---

## Part 8: Suggested MVP

Poetry in Motion MVP (12-week target hypothesis):

1. User: Nairobi woman, 25 to 40, buys fashion online sometimes, frustrated by fit and returns.
2. Job: "Help me find 3 outfits I would actually wear for work and weekends."
3. Flow: Quiz (persisted) to 12 curated SKUs from 5 verified local creators to M-Pesa checkout to delivery partner quoted at checkout.
4. Deferred: live sessions, subscriptions, trade-in logistics, global resale, 37 or more API routes.
5. Honest UI: "Beta. Styling suggestions are rule-based, not trained ML."

This MVP matches research pillars (representation, creators, intelligence) without pretending to match ThredUp, Stitch Fix, and TikTok Live simultaneously.

---

## Part 9: Additional Critical Review (June 2026)

This section records observations from the Phase 1 restructure process. It is a second pass at the research after all documents were read in full and reorganised.

### 9.1 The Research Structure Was Its Own Problem

The original folder layout (01-foundation, 02-market-intelligence, 03-technical-research) did not reflect the logical dependency between documents. A reader could enter at any layer without the context the previous layer was meant to provide. The geographic narrowing from global to Africa to Kenya was scattered across multiple files rather than structured as a deliberate sequence. This is not a minor formatting issue. A research structure that does not enforce reading order does not enforce thinking order. The restructure into a numbered pyramid with a mandatory reading sequence addresses this, but the underlying risk remains: if contributors add documents without following the sequence, the pyramid degrades back into a folder of notes.

Solved: CONTRIBUTING.md added to the Research repo. It requires every new document to state its dependencies and downstream documents explicitly, enforces folder rules, and includes a PR checklist covering notation standards, sustainability source requirements, and writing style.

### 9.2 The MVP Document Existed in Pieces but Not as a Decision

Before the restructure, MVP thinking was distributed across CRITICAL-REVIEW.md (Part 8), ENTITIES.md (Group 12), and FOUNDATION.md (Phase boundaries). None of these was a decision document. They were all recommendations. A recommendation is not a decision. The new 06-mvp/MVP.md consolidates these into a single wedge statement and a deferred list, but the wedge sentence itself is still marked as a hypothesis. Until the founder signs off on that sentence as a decision, Phase 1 is not complete regardless of how many documents exist.

Solved: sign-off field added to 06-mvp/MVP.md. Phase 2 engineering does not start until the field is filled.

### 9.3 DATA-ETHICS.md Is Correct in Principle but Unenforceable in Practice

The document states correct rules: minimum collection, opt-out, no false precision, no data sale, 30-day deletion. None of these rules has a corresponding technical control in the codebase. A rule without a control is a statement of intent, not a policy. The Kenya Data Protection Act 2019 does not accept statements of intent as compliance.

Recommendation: for each rule in DATA-ETHICS.md, Phase 2 must produce a corresponding technical control or a documented exception with a timeline. Example: "30-day deletion on account delete" requires a database-level cascade delete or a scheduled job. Neither exists yet.

Partially mitigated: image upload route confirmed as memory-only with no disk writes. File size limit of 5MB enforced. DATA-ETHICS control comment added to route. Explicit consent requirement for model training documented as Phase 2 gate. Remaining controls (30-day deletion, consent ledger, retention audit) require Phase 2 database.

### 9.4 ENTITIES.md Covers Global and Kenya but Skips the Middle

The entity map moves from global templates (Stitch Fix, ThredUp) directly to Kenya-native platforms (ShopZetu, Vivo). The East Africa layer, documented in EAST-AFRICA.md, has no corresponding entity research. There are no named logistics providers with quotes, no named EAC cross-border payment providers, and no named designers who sell across borders. EAST-AFRICA.md is currently a structural placeholder with correct observations but no named entities.

Recommendation: Phase 2 entity extensions must include at least one EAC-level entity in each of the following categories: logistics (cross-border courier), payments (multi-country mobile money), and creator (designer selling in two or more EAC markets).

### 9.5 The Reject List Has No Acceptance Criteria

LANDSCAPE.md Part 3.2 lists five patterns to reject: race-to-bottom price, opaque algorithms, bolt-on sustainability, platform rent extraction, and infinite scroll. These are stated as design principles. None has a measurable acceptance criterion. A principle without a criterion cannot be tested, and a principle that cannot be tested will be violated under deadline pressure without anyone noticing.

Solved: acceptance criteria added to LANDSCAPE.md Part 3.2 as a fifth column. Each criterion is a testable statement that can be checked in a code review or creator agreement audit.

### 9.6 The Research Is Still Single-Author

The critical review noted single-author bias in Phase 1. The restructure did not change this. All 13 documents were written or rewritten by one author. The pyramid structure is internally consistent precisely because one person built it, which means it has one person's blind spots throughout. The geographic narrowing from global to Kenya is well-executed, but it reflects one person's reading of the market. A Nairobi-based designer or shopper would likely contradict several assumptions in KENYA.md and ENTITIES.md on the basis of lived experience that desk research cannot replicate.

Recommendation: before Phase 2 engineering begins, at least two primary research interviews should be conducted: one with a Nairobi-based creator currently selling on social media, and one with a Nairobi-based woman in the target customer profile. The outputs should be written up as a document in 02-africa/ and used to challenge the assumptions in KENYA.md and 06-mvp/MVP.md directly.

---

## Part 10: Solved Problems

These problems were identified in earlier versions of this document and have since been resolved. They are recorded here to prevent regression.

| Problem | Original location | How it was solved | Solved in |
|---------|------------------|-------------------|-----------|
| Africa under-researched. Africa was one subsection in a global document. | Part 3, competitor blindness; Part 4.1, Western-centric history | Three dedicated documents created: 02-africa/AFRICA.md (continental), 02-africa/EAST-AFRICA.md (EAC regional), 02-africa/KENYA.md (city-level). Africa content extracted from LANDSCAPE.md and INDUSTRY-ECOMMERCE.md and INDUSTRY-FASHION.md. | Research restructure, June 2026 |
| Competitor blindness. ENTITIES.md was missing from the original structure. | Part 3, competitor blindness | 03-market-intelligence/ENTITIES.md written in full with 10 entity groups, competitive synthesis matrix, and entity-driven MVP wedge. Instagram and WhatsApp sellers named as the real incumbent. | Phase 1 research, May 2026 |
| Research structure did not enforce reading order. | Implicit in original folder layout | Numbered pyramid folder structure (00 through 06) with mandatory reading order table in README. Each document states its cross-references explicitly. | Research restructure, June 2026 |
| MVP thinking was distributed across multiple documents with no single decision point. | Part 8 (suggested MVP), ENTITIES.md Group 12, FOUNDATION.md phase boundaries | 06-mvp/MVP.md created as the apex document. Single wedge statement, deferred list, success criteria, and Phase 3 gate conditions. | Research restructure, June 2026 |
| DATA-ETHICS.md did not exist. Sensitive attributes had no governance document. | Part 6.5, ethics and legal | 00-foundation/DATA-ETHICS.md written with enforceable rules covering collection, opt-out, retention, images, sustainability data, and public demo rules. | Phase 1 research, May 2026 |
| This review was orphaned. Not linked from README. | Part 6.2, this review orphaned | README reading order table includes 05-critical-review/CRITICAL-REVIEW.md as step 12 in the mandatory sequence. | Research restructure, June 2026 |
| Research writing style used em dashes, rhetorical questions, and AI-generated prose patterns. | Implicit throughout original documents | All documents rewritten to technical research writing standards: full stops instead of em dashes, no rhetorical questions, no bold for emphasis in prose, consistent section numbering. | Research restructure, June 2026 |
| Wedge not chosen. MVP thinking was a hypothesis with no single decision sentence or deferred list. | Part 7, exit criteria; Part 6.1, strategy | 06-mvp/MVP.md written as the apex document. Wedge sentence defined, deferred list complete, success criteria and Phase 3 gate conditions documented. | Research restructure, June 2026 |
| v0 heritage. package.json name was my-v0-project. | Part 3, v0 heritage; Part 6.4, package name | Renamed to poetry-in-motion in package.json. | June 2026 |
| StyleAI branding in UI, manifest.json, metadata, and all UI strings. | Part 1, prototype honesty; Part 3, v0 heritage; Part 6.3, StyleAI branding | Global find-and-replace across all .tsx, .ts, .json, and .mjs files. All occurrences replaced with Poetry in Motion. | June 2026 |
| False AI. Image analysis returned hardcoded detectedStyle and confidence: 0.92 regardless of input. | Part 3, false AI; Part 6.3, fake AI confidence | confidence field removed from API response. Demo banner added to image upload page stating suggestions are rule-based, not trained ML. demoNotice field shown inline with results. | June 2026 |
| Security theatre. Base64 token auth in login and signup routes. | Part 3, security theatre; Part 6.4, Base64 auth | Both auth routes blocked in DEMO_MODE with a 403 response. Phase 2 comments added marking Base64 as not production auth and specifying the replacement: bcrypt plus Supabase Auth or Auth.js. Full replacement deferred to Phase 2 when database exists. | June 2026 |
| Fictional impact data. mock-data sustainability numbers; circular page showed CO2 and water without source. | Part 3, fictional impact data; Part 6.3, fake metrics | sustainabilitySourceId field added to Product type and set to null on all mock products. Sustainability impact API now refuses to accumulate CO2/water without a verified source ID, returning 422 with "Impact data not yet verified for this item." CO2/water fields removed from GET response. | June 2026 |
| Ethics without enforcement. Body type and skin tone collected with no consent language or opt-out enforcement. | Part 3, ethics without enforcement; Part 4.4, sensitive attributes | Consent language added to body type and skin tone quiz steps explaining purpose and no-sale policy. handleSubmit sanitises Prefer not to say to empty string before storing, ensuring it is excluded from recommendations and not stored as a category. Retention policy and audit remain Phase 2 database work. | June 2026 |
| No unit economics. No CAC, margin, return rate, take rate, or logistics cost modelled. | Part 3, no unit economics; Part 6.1, no unit economics | 03-market-intelligence/UNIT-ECONOMICS.md created. Known variables from Phase 1 research populated (Paystack fees, take rate range, LTV:CAC benchmarks, return rate range). Unknowns marked for Phase 2 measurement. Creator share contradiction (40 to 50% in copy versus 82 to 90% from take rate model) documented as a risk. | June 2026 |
| Movement language. Hero copy said "building a movement", claimed AI trained on African body types, showed 500+ unverified users, and stated 40 to 50% creator revenue share. | Part 3, movement language; Part 6.3, product | Hero description rewritten to transactional copy. "Building a movement" removed. AI feature card renamed to Style Quiz with honest description. Verified Sustainability card copy updated to note metrics shown only when verified. 500+ social proof replaced with Beta notice. Creator CTA revenue share percentage removed; replaced with "confirmed at onboarding". | June 2026 |
| Personalisation moat assumed. Recommendations route ignored quiz profile entirely and labelled algorithm as collaborative-filtering-v1. | Part 3, personalisation moat; Part 6.3, quiz not persisted | Recommendations route rewritten to read style profile from request header and score products by budget match, style preference match, creator presence, and stock. Algorithm relabelled rule-based-profile-match-v1 with honest notice. Phase 2 comment added for database lookup replacement. | June 2026 |
| Public-facing demo rules absent. No DEMO_MODE flag, fake CO2/water metrics visible, AI confidence score of 0.92 in production. | Part 7, exit criteria; Part 6.3, product; Part 6.4, technical | DEMO_MODE=true added to .env.local. Checkout blocked in orders POST when DEMO_MODE is true. CO2 and water metrics replaced with "Impact data not yet verified for this item." in circular page. confidence: 0.92 removed from AI image analysis route and replaced with demo notice. | June 2026 |

---

## Part 12: Remaining P0 Items

The following P0 items from Part 6 and the MVP Honesty Requirements are not yet resolved. They must be completed before any public repository or users.

- [ ] ODPC registration completed (MVP Honesty Requirement 6)
- [ ] Creator agreement template signed by all onboarded creators (MVP Honesty Requirement 7)
- [ ] One‑page strategy document created (Part 6.1) – see Research/06‑mvp/STRATEGY.md
- [ ] Link to CRITICAL‑REVIEW added to README (Part 6.2)
- [ ] Founder sign‑off on MVP wedge (MVP.md sign‑off field)
- [ ] Creator revenue share contradiction resolved (40‑50% vs 82‑90%)
- [ ] M‑Pesa checkout implementation (Paystack or Daraja API access)
- [ ] Primary research interviews (two interviews, write‑up in 02‑africa/PRIMARY‑RESEARCH.md)
- [ ] Technical infrastructure gates (database, auth, payments, creator payout rails)
- [ ] Legal and compliance gates (Kenya Data Protection Act compliance, pre‑owned authenticity policy, creator agreement draft, children’s data protection)
- [ ] Market validation gates (East Africa entity research, logistics partner, creator onboarding)
- [ ] Sign‑off checklist for Phase 2 start (all of the above)

## Summary

| Category | Assessment |
|----------|------------|
| Good | History, phase discipline, ethical intent, data model seeds, separated research, geographic narrowing now explicit, entities documented, MVP apex defined |
| Bad | Scope, fake AI and metrics, weak auth, no unit economics, Western quiz taxonomy |
| Weak | No primary research, no EAC-level entities, reject list has no acceptance criteria, MVP wedge not yet signed off |
| Limit | Logistics, trust, margins, incumbent WhatsApp commerce, single-author bias throughout |
| Fix | Sign off wedge, two primary interviews before Phase 2, technical controls for DATA-ETHICS rules, acceptance criteria for reject list, EAC entity research |

---

## References

- 01-global/LANDSCAPE.md Part 3.2 (reject list, needs acceptance tests)
- Stitch Fix public filings (personalisation does not equal automatic profitability)
- Kenya Data Protection Act 2019 (ODPC guidance on sensitive personal data)
- Ellen MacArthur Foundation (claims require traceability, not dashboard widgets alone)

---

## Part 11: Phase 2 Gates (Blockers Before Engineering Starts)

These problems cannot be solved in Phase 1 because they require decisions outside the scope of research, primary user data, or database infrastructure. Each gate requires a specific input before Phase 2 engineering begins.

### 11.1 Founder Sign-off on MVP Wedge

| Gate | Status | Blocker |
|------|--------|---------|
| MVP wedge decision (NAIROBI: 12 SKUs, 5 creators, quiz-to-checkout flow) | Defined in 06-mvp/MVP.md | Requires signature on Part 8 sign-off field |
| Creator revenue share confirmation | 40 to 50% stated in copy but 82 to 90% in unit economics model; contradiction must be resolved | Requires: creator agreement draft, COG analysis, margin model validation |
| M-Pesa checkout implementation | Documented as necessary in FOUNDATION and EAST-AFRICA | Requires: Paystack or M-Pesa API access, test account, compliance review |

### 11.2 Primary Research Gates

These require at least two user interviews before Phase 2 code begins.

| Gate | Status | Blocker |
|------|--------|---------|
| Creator interview: Nairobi-based social seller | Assumed in ENTITIES and EAST-AFRICA | Requires: one 1-hour recorded interview, write-up challenging KENYA.md assumptions |
| Customer interview: Nairobi woman, 25-40 | Assumed in MVP and FOUNDATION | Requires: one 1-hour recorded interview, quiz prototype test, fit outcome feedback |

### 11.3 Technical Infrastructure Gates

These require database, auth, and payment systems before certain features ship.

| Gate | Status | Blocker |
|------|--------|---------|
| DATABASE: User identity and quiz persistence | Currently: in-memory, lost on reload | Requires: Postgres or Supabase setup, auth.js or Supabase Auth integration |
| DATA-ETHICS enforcement: 30-day deletion | Currently: no database, no audit trail | Requires: cascade delete schema, retention policy, audit logging, legal review |
| Payment processing: M-Pesa and credit card checkout | Currently: mocked, no transactions | Requires: Paystack or equivalent integration, PCI compliance review |
| Creator payout rails: Tax ID collection, monthly payouts | Currently: no KYC, no payment processor | Requires: creator KYC form, tax ID validation, payout schedule, dispute flow |

### 11.4 Legal and Compliance Gates

| Gate | Status | Blocker |
|------|--------|---------|
| Kenya Data Protection Act compliance | DATA-ETHICS.md drafted but not audited | Requires: legal review by Kenya-qualified data protection attorney, audit report |
| Pre-owned / trade-in authenticity policy | Currently: no authentication mechanism | Requires: authentication SOP, dispute resolution process, insurance or guarantee terms |
| Creator agreement draft | Currently: no contract exists | Requires: agreement draft covering revenue share, IP ownership, dispute resolution, term |
| Children's data protection | Currently: no age gate in code or research | Requires: age verification mechanism, parental consent flow (if under 18 supported) |

### 11.5 Market Validation Gates

These require real transaction data or partner commitments before scaling.

| Gate | Status | Blocker |
|------|--------|---------|
| East Africa entity research: at least 3 named partners | Currently: EAC layer researched but no named entities | Requires: conversations with 2+ logistics providers, 1+ regional payment provider, quotes, MOUs if possible |
| Logistics partner: quotes and COD capability | Currently: no partner, costs assumed | Requires: 3+ quote comparison, test shipment, failure mode documentation |
| Creator onboarding: 5+ actual creators with inventory | Currently: 2 mock creators, no real inventory | Requires: creator recruitment, inventory uploads, first real sale or trade session |

### 11.6 Sign-Off Checklist for Phase 2 Start

Phase 2 engineering begins only after all of the following are complete:

- [ ] 06-mvp/MVP.md signed off by founder (Part 8 sign-off field filled)
- [ ] Unit economics contradictions resolved (40-50% vs 82-90% creator share decided)
- [ ] Two primary user interviews completed and written up as 02-africa/PRIMARY-RESEARCH.md
- [ ] Kenya data protection legal review completed and filed
- [ ] One named M-Pesa or Paystack contact confirmed for Phase 2
- [ ] Draft creator agreement reviewed by finance and legal
- [ ] Age gate and children's data handling documented

Until all are checked, Phase 1 is still in motion.

