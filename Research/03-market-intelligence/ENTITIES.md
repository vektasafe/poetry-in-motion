# Poetry in Motion: Entity Intelligence

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Living document, Phase 1 deep entity research (May 2026)
Scope: Market participants whose strategies, economics, or infrastructure define the terrain for Poetry in Motion
Cross-reference: 02-africa/KENYA.md, 01-global/LANDSCAPE.md, 01-global/INDUSTRY-ECOMMERCE.md, 01-global/INDUSTRY-FASHION.md, 04-technical-research/OPEN-SOURCE-REFERENCE.md, 05-critical-review/CRITICAL-REVIEW.md

---

## How to Read This Document

Each entry uses a fixed structure for consistent comparison.

| Section | Purpose |
|---------|---------|
| Entity profile | What it is, ownership, geography, scale signals |
| Business model and economics | How money is made; take rates; constraints |
| Technology and operations | Stack patterns, logistics, data and AI |
| Overlap with Poetry in Motion | Map to five pillars: quiz/AI, creators, circular, Africa, ethics |
| Classification | COMPETITOR, COMPLEMENT, TEMPLATE, INFRASTRUCTURE, REGULATOR, or AVOID |
| Poetry in Motion response | Borrow, partner, or differentiate |
| Documentation status | CONFIRMED (primary source), REPORTED (press or analyst), INFERRED |

The real incumbent in Kenya fashion is social commerce, not Jumia. The entity map is structured to reflect that.

---

## Entity Map

```
                    GLOBAL PRICE AND VOLUME PRESSURE
                    Shein, Temu, Amazon (ZA), ASOS
                              |
                    PAN-AFRICAN MARKETPLACES
                    Jumia, Kilimall, Takealot
                              |
         _____________________|_____________________
        |                     |                     |
   SOCIAL                KENYA FASHION-NATIVE   PERSONALISATION
   WhatsApp              ShopZetu, Vivo, ANKA   Stitch Fix
   Instagram             (formal platforms)     (US, template)
   TikTok
        |                     |
        |              POETRY IN MOTION
        |_____________ quiz, creators,
                       circular, M-Pesa
                              |
              ________________|________________
             |                |                |
          PAYMENTS        LOGISTICS        REGULATORS
          M-Pesa          Jumia last mile  ODPC, CAK
          Paystack        (Sendy: failed)  Kenya e-commerce
          Flutterwave                      policy (draft)
```

---

## Group 1: Personalisation and Styling (Global Templates)

### Entity 1.1: Stitch Fix, Inc. (NASDAQ: SFIX)

#### Entity profile

| Field | Detail |
|-------|--------|
| Founded | 2011, San Francisco |
| Model | Online personal styling: human stylists plus algorithms |
| Markets | United States (primary) |
| Scale (FY2026 Q1) | Approximately 2.31 million active clients; net revenue 342.1 million USD per quarter, up 7.3% year on year |
| RPAC | 559 USD net revenue per active client, up 5.3% year on year |
| Products | Fix (curated box), Freestyle (on-demand shop), GenAI Vision style assistant |

CONFIRMED: SFIX Q1 FY2026 earnings; 10-K 2025.

#### Business model and economics

Revenue comes from retail markup on apparel, footwear, and accessories plus styling engagement. The model is wholesale buy then retail sell. The flywheel is style profile leading to Fix or Freestyle, then keep or return feedback feeding model improvement. Active clients declined for years before a turnaround bet on GenAI and stylist hybrid in 2025 to 2026. Personalisation without client count growth can still raise revenue per active client, but CAC and inventory risk remain significant.

#### Technology and operations

Billions of fit and style data points from returns and feedback. GenAI for outfit visualisation and conversational styling launched in 2025. Physical fulfillment with inventory ownership and reverse logistics for returns.

#### Overlap with Poetry in Motion

| Pillar | Overlap |
|--------|---------|
| Quiz and profile | High. Direct analog to /quiz. |
| AI | High. Stitch Fix has real data; Poetry in Motion has mocks. |
| Creators | Low. National brands and private label, not African makers. |
| Circular | Medium. Returns are a cost centre, not a circular module. |
| Africa | None. |

#### Classification

TEMPLATE (product model). AVOID (inventory-heavy clone).

#### Poetry in Motion response

Borrow: quiz to persisted profile to recommendations; stylist and AI hybrid positioning; keep or return feedback loop design.
Reject: owning inventory at MVP; US-only size taxonomy without localisation.
Differentiate: African creators, representation, circularity, marketplace not warehouse-first.

#### Documentation status: CONFIRMED (SEC filings)

---

## Group 2: Ultra-Fast and Global Fashion Commerce

### Entity 2.1: Shein (private, Singapore HQ narrative)

#### Entity profile

| Field | Detail |
|-------|--------|
| Founded | 2008, China; global ultra-fast fashion |
| Model | Mobile-first; thousands of SKUs per day; test-and-reorder supply chain |
| Africa | Active in Kenya, South Africa, Ghana, and Nigeria via app; influencer-led |
| Pressure | Cited as threat to local textile jobs. Over 34,000 jobs at risk by 2030 in South Africa projections (REPORTED). |

REPORTED: High Street Journal; MoonLook Africa.

#### Business model and economics

Extreme SKU velocity, social ads, low FOB cost, and cross-border parcel post. The moat is supply chain plus ad spend plus algorithmic trend detection, not brand loyalty. In Kenya, cross-border customs duties of 30 to 35% on clothing apply (REPORTED, industry debate).

#### Overlap with Poetry in Motion

Shein is the antithesis of every ethical pillar. There is no overlap.

#### Classification

COMPETITOR (price anchor). AVOID (model).

#### Poetry in Motion response

Never compete on SKU count, price, or speed. Counter-position on curated local creators, fit and intent, circularity, and transparent verified impact. Monitor Kenya tariff and enforcement policy affecting cross-border fashion.

#### Documentation status: REPORTED

---

### Entity 2.2: Temu (PDD Holdings)

#### Entity profile

| Field | Detail |
|-------|--------|
| Parent | PDD Holdings, approximately 34.9 billion USD revenue 2023 (REPORTED) |
| Africa | Nigeria launch November 2024; aggressive vouchers; competes with Jumia |
| Model | General merchandise plus fashion; gamified app; cross-border |

REPORTED: Semafor on Jumia versus Temu and Shein; Rest of World.

#### Classification

COMPETITOR (GMV attention). AVOID (ethics and positioning).

#### Poetry in Motion response

Same as Shein: relevance, trust, and local makers, not infinite cheap SKUs.

---

## Group 3: Resale and Circular Fashion

### Entity 3.1: ThredUp, Inc.

#### Entity profile

| Field | Detail |
|-------|--------|
| Model | Managed resale: consumer sends bag; ThredUp photographs, lists, and ships |
| Global secondhand (2025) | Approximately 257 billion USD; approximately 10% of apparel spend (REPORTED, GlobalData via ThredUp) |
| 2030 projection | Approximately 393 billion USD global secondhand |
| Primary constraint | Supply of quality used inventory, not demand |

CONFIRMED: ThredUp IR April 2026.

#### Business model and economics

Commission is dynamic at approximately 20 to 95% of sale price by brand and price tier, with higher percentage on low-ticket items. Processing cost per SKU is significant at scale. Brand partners such as Gap and H&M programs feed supply through Resale as a Service (RaaS).

#### Overlap with Poetry in Motion

| Pillar | Overlap |
|--------|---------|
| Circular | High. Trade-in and pre-owned narrative. |
| AI | High. Discovery in resale feeds. |

#### Classification

TEMPLATE (circular operations). COMPETITOR (if Poetry in Motion does resale without operations).

#### Poetry in Motion response

Borrow: treat supply as bottleneck; easy seller onboarding; AI discovery.
Reject: opening circular UI without intake, grading, and pricing partners.
Partner path: RaaS-style brand tie-ins with Kenyan designers in Phase 3.

---

### Entity 3.2: Vinted, Depop, Poshmark (peer-to-peer resale)

| Entity | Seller fees | Monetisation | Classification |
|--------|-------------|--------------|----------------|
| Vinted | 0% seller commission | Buyer protection fee plus bumps | TEMPLATE (supply growth) |
| Depop | 0% seller (2024 shift) | Buyer-side fees | COMPETITOR (social resale UX) |
| Poshmark | Seller fees (varies) | Social marketplace | TEMPLATE |

REPORTED: Fashion marketplace fee statistics; Brand Panic on fee shifts.

Poetry in Motion response: if enabling C2C resale, prefer buyer-side or promotion fees over seller margin compression. Social graph matters more than web storefront alone.

---

## Group 4: Kenya Fashion-Native Platforms

### Entity 4.1: ShopZetu Ltd.

#### Entity profile

| Field | Detail |
|-------|--------|
| Founded | 2021, Nairobi |
| Founders | Marvin Kiragu; Wandia Gichuru (co-founder Vivo Activewear) |
| Funding | 1 million USD pre-seed (2023): Chui Ventures, Launch Africa, others |
| Vendors | Over 300, targeting 1,000; over 20,000 SKUs listed |
| Customers served | Over 30,000 (REPORTED, 2023) |
| Expansion | Rwanda, Tanzania, Uganda trials |

CONFIRMED: TechCrunch; Business of Fashion.

#### Business model and economics

Multi-brand lifestyle marketplace for the African consumer, not export-first. Revenue from sales commission, delivery, and value-added services. Free vendor onboarding. Stated problem: fragmented Instagram and WhatsApp sellers with no price visibility or trust.

#### Overlap with Poetry in Motion

| Pillar | Overlap |
|--------|---------|
| Discovery | High. Same TAM. |
| Creators | Medium. Brands as vendors, not voting or production lifecycle. |
| AI and quiz | Low in public positioning. |
| Africa | Very high. |

#### Classification

COMPETITOR (primary Kenya peer).

#### Poetry in Motion response

Must articulate a clear wedge: AI styling plus circular plus creator production voting versus another fashion mall. Potential partnership: list curated creator drops on ShopZetu versus building a parallel catalog. This is a strategic choice for Phase 2. Learn from founder distribution via Vivo retail footprint.

#### Documentation status: CONFIRMED

---

### Entity 4.2: Vivo Activewear (Vivo Fashion Group)

#### Entity profile

| Field | Detail |
|-------|--------|
| Founder | Wandia Gichuru |
| Model | Kenyan fashion brand; over 20 stores; Rwanda presence; targeting 30 stores |
| Spin-off | ShopZetu as separate online aggregation play |

CONFIRMED: Stanford GSB case interview.

#### Classification

COMPLEMENT (supply). TEMPLATE (omnichannel).

#### Poetry in Motion response

Creator onboarding playbook: designers with physical and digital presence. Not a platform competitor unless ShopZetu absorbs the styling narrative.

---

### Entity 4.3: ANKA (formerly Afrikrea)

#### Entity profile

| Field | Detail |
|-------|--------|
| Founded | 2016, Cote d'Ivoire, pan-African |
| Model | Shop, Pay, and Ship for Made of Africa products |
| Sellers | Over 7,000 from 47 countries; approximately 20,000 merchants cited in IFC round (REPORTED) |
| Funding | 13.5 million USD total; 5 million USD IFC and Proparco extension (REPORTED) |
| Logistics | DHL integration from Africa; global buyers |

CONFIRMED: ANKA; Choose Africa and IFC.

#### Business model and economics

Export-oriented DTC for African makers, contrasting with ShopZetu's local lifestyle focus. Monetises shipping, payments, and shop SaaS.

#### Classification

COMPETITOR (African maker platform). TEMPLATE (cross-border ship and pay).

#### Poetry in Motion response

Differentiate: Kenya and East Africa domestic styling plus circular first. ANKA is export rails. Borrow: unified pay and ship narrative for creators who also sell abroad in Phase 3.

---

### Entity 4.4: The Folklore Group

#### Entity profile

| Field | Detail |
|-------|--------|
| Founded | 2018, US and Africa diaspora focus |
| Pivot | DTC to B2B wholesale (Folklore Connect, 2022) |
| Funding | 6.2 million USD total; 3.4 million USD seed 2024 |
| Retail partners | Nordstrom, Saks, Bergdorf Goodman (REPORTED) |
| Services | Wholesale SaaS, PO financing, talent marketplace |

CONFIRMED: TechCrunch 2024.

#### Classification

TEMPLATE (creator B2B). COMPLEMENT (export path for creators).

#### Poetry in Motion response

Poetry in Motion consumer plus creator voting is not wholesale SaaS. These are different layers. Later: wholesale module for creators who graduate to global retail.

---

### Entity 4.5: Industrie Africa and Jendaya

| Entity | Role |
|--------|------|
| Industrie Africa | Encyclopedia plus e-commerce; sustainability filters; UK and US clientele (REPORTED, Vogue) |
| Jendaya | Luxury African fashion e-commerce (REPORTED, sector roundups) |

Classification: TEMPLATE (storytelling and filters). Not Kenya mass-market competitors.

---

## Group 5: Global Personalisation Templates

### Entity 5.1: Farfetch (acquired by Coupang 2024)

Distributed inventory model connecting boutiques globally with centralised discovery. Demonstrated that luxury fashion e-commerce requires curation, authentication, and premium logistics. Relevant as a template for creator-distributed catalog, not as a direct competitor.

Classification: TEMPLATE (distributed inventory model).

---

## Group 6: Open-Source and Enterprise Commerce

Full matrix: 04-technical-research/OPEN-SOURCE-REFERENCE.md.

| Entity | Stars | Relation to Poetry in Motion |
|--------|-------|------------------------------|
| Medusa | Approximately 34,000 | TEMPLATE for TypeScript commerce core |
| Saleor | Approximately 23,000 | TEMPLATE for GraphQL and OMS |
| ERPNext plus LS Shop | ERP approximately 35,000 | TEMPLATE for apparel variants (SAC/SAV) |
| Spryker | Open code | AVOID at MVP (license) |

Classification: INFRASTRUCTURE and TEMPLATE. Not market competitors.

---

## Group 7: Competitive Synthesis Matrix

| Entity | Threat to Poetry in Motion | Partner potential | Learn | Ignore at MVP |
|--------|---------------------------|-------------------|-------|---------------|
| Instagram and WhatsApp sellers | Very high | High | Social-first GTM | No |
| ShopZetu | High | Medium | Kenya fashion mall | No |
| Jumia | Medium | Medium | Logistics | Low |
| Shein and Temu | High | None | Nothing | High |
| Stitch Fix | Low | None | Quiz and AI loop | Medium |
| ThredUp and Vinted | Medium | Low | Circular supply | High |
| ANKA | Medium | Medium | Export rails | Low |
| The Folklore | Low | Medium | B2B wholesale | High |
| Paystack and M-Pesa | None | Very high | Payments | No |
| Sendy | None | None | Failure modes | Always |

---

## Group 8: Entity-Driven MVP Wedge

The entity map produces the following MVP recommendation.

| Choice | Entity logic |
|--------|--------------|
| Customer | Nairobi woman already buying via Instagram and M-Pesa |
| Supply | 5 to 10 creators also selling on social (upgrade path) |
| Channel | Web app plus WhatsApp share and checkout |
| Payments | Paystack M-Pesa (Phase 2) |
| Logistics | Partner courier or creator-managed until volume |
| Defer | National marketplace scale, managed resale warehouse, export paths |

---

## Phase 2 Entity Research Extensions

- [ ] Primary research: 10 creator interviews, 10 shopper interviews in Nairobi
- [ ] Entity deep dive: Copia Global, Masoko, Sky.Garden (Kenya)
- [ ] Logistics quotes: 3 couriers for fashion parcel delivery
- [ ] TikTok Shop Kenya fee schedule (primary source)
- [ ] ODPC registration checklist for Poetry in Motion data map

---

## Master Source Bibliography

| Topic | Sources |
|-------|---------|
| Kenya marketplaces | TechCrunch, Business of Fashion, Eagle News, Jumia Group PDF, ECDB |
| Global styling | SFIX SEC filings |
| Resale | ThredUp IR 2026 |
| Shein and Temu Africa | Semafor, Rest of World, High Street Journal |
| Payments | Paystack, Flutterwave, CNBCode |
| Logistics | WEF, Tekedia |
| African designers | Vogue, TechCrunch (Folklore), ANKA, IFC |
| Regulation | ODPC, DLA Piper, Digital Policy Alert |
| Open source | GitHub API May 2026, OPEN-SOURCE-REFERENCE.md |

Document maintenance: update quarterly or when a major entity event occurs such as funding, shutdown, or Kenya policy change.
