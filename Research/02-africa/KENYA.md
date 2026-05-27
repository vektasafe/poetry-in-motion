# Poetry in Motion: Kenya E-Commerce and Fashion

Author: James Kabingu, Vektasafe
Status: Phase 1 market intelligence, web-sourced and confirmed where noted
Scope: Kenya-specific e-commerce, fashion, payments, logistics, and regulatory context
Cross-reference: 02-africa/EAST-AFRICA.md, 03-market-intelligence/ENTITIES.md, 00-foundation/DATA-ETHICS.md
Last updated: May 2026

---

## 1. Kenya as the Primary Market

Kenya is the most developed digital commerce market in East Africa and the primary target for Poetry in Motion's MVP. The rationale is not arbitrary. Kenya has the highest mobile money penetration in the region, the most active fashion creator community in East Africa, the most developed regulatory framework for data protection, and the largest urban middle-class consumer base for fashion in the region.

Nairobi is the specific launch city. The MVP customer is a Nairobi woman aged 25 to 40 who buys fashion online sometimes and is frustrated by fit and returns.

---

## 2. Kenya E-Commerce Market

| Metric | Estimate | Source |
|--------|----------|--------|
| SIM penetration | Over 143% (March 2025) | Reported, Knickpoint Media |
| TikTok ad reach growth | Plus 4.53 million users year on year in Kenya (2024 to 2025) | Reported, Knickpoint Media |
| Jumia Kenya sales (2025) | KSh 15.8 billion, approximately 122.8 million USD | Reported, Eagle News Feed |
| Jumia Kenya share of group GMV | Approximately 15% (2025) | Reported |
| Jumia rural orders | Approximately 60% from secondary cities and rural areas (2025) | Confirmed, Jumia rural report |

Social commerce is the dominant channel. More than 80% of online shoppers use social media to discover and buy. WhatsApp Business catalog plus M-Pesa person-to-person transfer is the default transaction stack for informal sellers.

---

## 3. Kenya Fashion Market

### 3.1 Formal Platforms

ShopZetu is the closest formal Kenya fashion marketplace peer to Poetry in Motion. Founded 2021 in Nairobi by Marvin Kiragu and Wandia Gichuru (co-founder of Vivo Activewear). Raised 1 million USD pre-seed in 2023. Over 300 vendors targeting 1,000. Over 20,000 SKUs listed. Over 30,000 customers served as of 2023. Expanding to Rwanda, Tanzania, and Uganda.

ShopZetu's stated problem is the same as Poetry in Motion's supply-side problem: fragmented Instagram and WhatsApp sellers with no price visibility or trust infrastructure.

Vivo Activewear is a Kenyan fashion brand with over 20 stores and a Rwanda presence. It is a template for omnichannel creator-to-retail progression, not a direct platform competitor.

### 3.2 Informal Sellers

The real incumbent in Nairobi fashion commerce is the informal social seller. Representative archetypes:

| Archetype | Example pattern | Scale signal |
|-----------|-----------------|--------------|
| CBD thrift | Bolt Fashions | Over 46,000 Instagram followers; trust via DMs |
| Phone to shop | Holopio | TikTok over 20,000 followers, then physical shop |
| Gikomba and Toi market | Offline supply for social sellers | Inventory source for pre-owned and thrift |

These sellers are not the competition to defeat. They are the creator onboarding pool. Poetry in Motion's value proposition to them is logistics, payments, and discovery infrastructure they currently lack.

### 3.3 Kenya Fashion Creator Ecosystem

Nairobi has active designer communities producing ready-to-wear, occasion wear, and streetwear. Key characteristics:

- Small-batch production is the norm. Most designers cannot fulfil orders above 50 to 100 units without external manufacturing support.
- Fabric sourcing is mixed: local kitenge and ankara, imported polyester and cotton blends.
- Pricing is mid-market relative to global standards but premium relative to Shein and Temu cross-border imports.
- Brand identity is strong on social media. Formal e-commerce presence is weak.

---

## 4. Kenya Payments

### M-Pesa (Safaricom Daraja API)

M-Pesa is the dominant mobile money platform. STK Push checkout is the standard consumer payment flow. Integration options are direct Daraja (high volume, lowest fees) or via aggregators.

Classification: Infrastructure. Mandatory for any Kenya-first commerce platform.

### Paystack (Stripe-owned)

Live for all merchants in Kenya. Supports cards, M-Pesa at 1.5%, and Apple Pay. Card rates: 2.9% local, 3.8% international. Strong developer documentation, Shopify and WooCommerce plugins, and split payment support for creator payouts.

Classification: Infrastructure. Recommended for Phase 2 MVP checkout.

### Flutterwave

Supports M-Pesa, Airtel Money, cards, and bank transfer in Kenya. Multi-country Africa expansion capability.

Classification: Infrastructure. Alternative or complement to Paystack for multi-country Phase 3.

### Recommendation

Use Paystack for Phase 2 MVP. Plan Daraja direct integration at volume. Use Paystack Split or Flutterwave subaccounts for creator payout splitting.

---

## 5. Kenya Logistics

### Current Landscape

Sendy ceased operations in September 2023 after failing to sustain asset-light logistics at scale. This is the primary cautionary tale for Poetry in Motion. Do not build national fulfillment dependency before product-market fit.

Jumia Logistics operates pickup stations (over 300 in Kenya narrative) and last-mile delivery for marketplace sellers. It is a potential partner, not a competitor.

Other providers requiring RFQ in Phase 2: Fargo, G4S, Speedball. DHL is confirmed for export path following the ANKA model.

### Recommendation

Start with creator-managed delivery or a single courier partner for Nairobi urban delivery. Obtain logistics quotes from at least three couriers in Phase 2 before committing to any provider.

---

## 6. Kenya Regulatory Environment

### Office of the Data Protection Commissioner (ODPC)

The Data Protection Act 2019 and 2021 Regulations require registration as a data controller or processor, explicit consent for data collection, a Data Protection Impact Assessment for sensitive data, and breach notification. Style quiz fields including body type, skin tone, and photos are high compliance surface areas.

Classification: Regulator. Mandatory compliance before public launch.

### Competition Authority of Kenya (CAK)

The CAK investigated online food and delivery platforms in 2024 on data consent and market power grounds. The Consumer Protection Act 2012 covers misleading green claims and refund rights.

Classification: Regulator. Monitor for sustainability claim rules.

### Kenya National E-Commerce Policy (draft)

A national e-commerce policy is in development, covering trustmark, seller identity, and consumer protection in response to Shein and Temu cross-border activity. Track for sustainability claim rules.

Classification: Emerging regulator.

---

## 7. Kenya-Specific Implications for Poetry in Motion

| Priority | Implication |
|----------|-------------|
| P0 | Register with ODPC before collecting any user data |
| P0 | WhatsApp order status and M-Pesa payment links are not optional features |
| P0 | Shareable quiz results for social distribution |
| P1 | Paystack M-Pesa integration for checkout |
| P1 | Creator onboarding: target top social sellers as first verified creators |
| P1 | Logistics: partner courier or creator-managed until volume |
| P1 | Obtain logistics quotes from three couriers covering Nairobi urban delivery |
| P2 | Monitor Kenya e-commerce policy for sustainability claim rules |
| P2 | TikTok Shop Kenya fee schedule: obtain primary source |

---

## 8. Phase 2 Research Extensions

- [ ] Primary research: 10 creator interviews, 10 shopper interviews in Nairobi
- [ ] Entity deep dive: Copia Global, Masoko, Sky.Garden
- [ ] Logistics quotes: 3 couriers for fashion parcel delivery in Nairobi
- [ ] TikTok Shop Kenya fee schedule (primary source)
- [ ] ODPC registration checklist for Poetry in Motion data map

---

## 9. Source Bibliography

| Source | URL |
|--------|-----|
| Knickpoint TikTok Kenya 2025 | https://www.knickpointmedia.co.ke/tiktok-shop-kenya-2025-social-commerce-revolution-e-commerce-growth/ |
| Eagle News Feed Jumia Kenya | https://eaglenewsfeed.com/jumia-kenya-records-sh15-8bn-sales-as-year-end-demand-surges/ |
| Jumia rural report | https://group.jumia.com/download/files/community/articles/jumia-kenyas-2nd-rural-e-commerce-report-expanding-access-driving-inclusion-connection-border-to-border-1771847915.pdf |
| TechCrunch ShopZetu | https://techcrunch.com/2023/06/27/shopzetu-raises-pre-seed-funding-to-fuel-growth-of-its-fashion-marketplace-beyond-kenya/ |
| Paystack Kenya | https://paystack.com/blog/company-news/kenya |
| Flutterwave Kenya | https://flutterwaveinc.mintlify.app/supported-countries/kenya |
| ODPC | https://www.odpc.go.ke/ |
| DLA Piper Kenya data protection | https://www.dlapiperdataprotection.com/?c=KE&t=law |
| Tekedia Sendy shutdown | https://www.tekedia.com/kenyan-logistics-startup-sendy-shuts-down-operations-explores-sales-of-assets/ |
| Stanford GSB Vivo case | https://www.gsb.stanford.edu/insights/pivot-adapt-grow-building-fashion-brand-kenya |

Next in pyramid: 03-market-intelligence/ENTITIES.md.
