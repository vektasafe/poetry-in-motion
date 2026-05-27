# Poetry in Motion: Unit Economics

Author: James Kabingu, Vektasafe
Status: Phase 1 draft. Variables sourced from research. Unknowns marked for Phase 2 validation.
Cross-reference: 02-africa/KENYA.md, 03-market-intelligence/ENTITIES.md, 06-mvp/MVP.md
Last updated: June 2026

---

## Purpose

This document sets up the unit economics model for Poetry in Motion. It records what is known from Phase 1 research, what must be assumed for planning, and what must be measured from real transactions in Phase 2. No number in this document should be treated as validated until it is marked [MEASURED].

---

## Notation

- [KNOWN]: sourced from confirmed or reported research in Phase 1 documents
- [ASSUMED]: reasonable estimate pending Phase 2 validation
- [UNKNOWN]: must be measured from real transactions or primary research

---

## 1. Revenue Model

Poetry in Motion earns commission on GMV from creator sales. The platform does not own inventory.

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Take rate (platform commission) | 10 to 18% of sale price | [ASSUMED] | INDUSTRY-ECOMMERCE.md: sustainable range for fashion marketplaces |
| Creator share | 82 to 90% of sale price after platform commission | [ASSUMED] | Derived from take rate above |
| Subscription revenue | Not in MVP | [KNOWN] | 06-mvp/MVP.md deferred list |

---

## 2. Per-Order Cost Structure

### 2.1 Payment Processing

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Paystack M-Pesa fee | 1.5% of transaction value | [KNOWN] | KENYA.md, Paystack Kenya confirmed |
| Paystack local card fee | 2.9% of transaction value | [KNOWN] | KENYA.md, Paystack Kenya confirmed |
| Paystack international card fee | 3.8% of transaction value | [KNOWN] | KENYA.md, Paystack Kenya confirmed |
| Refund fee | Full fee retained by Paystack on refund | [ASSUMED] | Standard Paystack policy |

### 2.2 Logistics

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Nairobi urban delivery cost | Unknown | [UNKNOWN] | Phase 2: obtain quotes from 3 couriers |
| Creator-managed delivery cost | Absorbed by creator | [ASSUMED] | MVP default before courier partner |
| Return shipping cost | Unknown | [UNKNOWN] | Phase 2: measure from first 50 orders |
| COD fraud rate | Unknown | [UNKNOWN] | Phase 2: measure from first 50 orders |

### 2.3 Returns

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Fashion online return rate | 20 to 40% | [KNOWN] | INDUSTRY-FASHION.md: industry range |
| Poetry in Motion return rate | Unknown | [UNKNOWN] | Phase 2: measure from first 50 orders |
| Cost per return (processing) | Unknown | [UNKNOWN] | Phase 2: measure from first 50 orders |

---

## 3. Per-Order Contribution Margin Model

This model uses assumed values. Replace with [MEASURED] values as Phase 2 data arrives.

```
Average Order Value (AOV)                        [UNKNOWN]
  minus  Platform commission (15% assumed)        [ASSUMED]
  =      Net revenue to platform per order

Net revenue to platform
  minus  Paystack M-Pesa fee (1.5% of AOV)       [KNOWN]
  minus  Logistics cost per order                 [UNKNOWN]
  minus  Return cost (return rate x cost/return)  [UNKNOWN]
  minus  Customer support cost per order          [UNKNOWN]
  =      Contribution margin per order
```

Phase 2 must produce a real AOV from the first 50 orders before this model can be validated.

---

## 4. Customer Acquisition Cost (CAC)

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Organic CAC (social sharing, quiz) | Unknown | [UNKNOWN] | Phase 2: measure from first 200 users |
| Paid CAC (Instagram, TikTok ads) | Unknown | [UNKNOWN] | Phase 2: measure if paid acquisition used |
| Target LTV:CAC ratio | Greater than 3x on contribution basis | [KNOWN] | INDUSTRY-ECOMMERCE.md: healthy marketplace benchmark |
| Target CAC payback period | Under 12 months | [KNOWN] | INDUSTRY-ECOMMERCE.md: healthy marketplace benchmark |

---

## 5. Creator Economics

| Variable | Value | Status | Source |
|----------|-------|--------|--------|
| Creator share of sale price | 82 to 90% | [ASSUMED] | Derived from 10 to 18% platform take rate |
| Creator production cost per unit | Unknown | [UNKNOWN] | Phase 2: creator onboarding interviews |
| Creator gross margin per unit | Unknown | [UNKNOWN] | Phase 2: creator onboarding interviews |
| Minimum viable creator GMV per month | Unknown | [UNKNOWN] | Phase 2: creator onboarding interviews |

The 40 to 50% creator share referenced in early product copy is not consistent with a 10 to 18% platform take rate. If the platform takes 10 to 18%, the creator receives 82 to 90%, not 40 to 50%. The 40 to 50% figure may refer to a revenue share on platform-owned inventory, which is not the MVP model. This contradiction must be resolved before any public creator agreement is signed.

---

## 6. Viability Thresholds

These are the minimum conditions under which the MVP model is solvent. All are [ASSUMED] pending Phase 2 data.

| Threshold | Assumed value | What breaks it |
|-----------|---------------|----------------|
| Minimum AOV for positive contribution margin | KSh 2,500 (approximately 19 USD) | High return rate or high logistics cost |
| Maximum return rate before negative margin | 25% | Depends on AOV and logistics cost |
| Minimum monthly orders for platform sustainability | Unknown | Requires real CAC and fixed cost data |
| Minimum creator GMV per month to retain creator | Unknown | Requires creator interview data |

---

## 7. What Phase 2 Must Measure

Phase 2 is not complete on unit economics until the following are filled in with [MEASURED] values:

- [ ] AOV from first 50 orders
- [ ] Return rate from first 50 orders
- [ ] Logistics cost per order from courier partner
- [ ] CAC from first 200 users
- [ ] Creator production cost per unit from at least 3 creator interviews
- [ ] Contribution margin per order calculated from real data
- [ ] LTV:CAC ratio calculated from real cohort

---

## 8. Known Risks to the Model

| Risk | Detail |
|------|--------|
| M-Pesa fees plus refunds | A 1.5% payment fee plus a full-fee retention on refunds compresses margin on low-AOV orders significantly |
| High return rate | Fashion return rates of 20 to 40% can eliminate contribution margin entirely on orders below KSh 3,000 |
| Creator share contradiction | The 40 to 50% creator share in product copy is inconsistent with a marketplace take rate model. Must be resolved before creator agreements are signed. |
| No fixed cost model | Server, support, and operational fixed costs are not modelled here. Phase 2 must add these. |
| COD fraud | Cash on delivery fraud is a documented risk in Kenya e-commerce. Rate is unknown until measured. |

---

## References

- 01-global/INDUSTRY-ECOMMERCE.md: take rates, LTV:CAC benchmarks
- 01-global/INDUSTRY-FASHION.md: return rates, channel economics
- 02-africa/KENYA.md: Paystack fees, logistics context
- 03-market-intelligence/ENTITIES.md: creator share context
- 06-mvp/MVP.md: MVP scope and Phase 2 exit criteria
