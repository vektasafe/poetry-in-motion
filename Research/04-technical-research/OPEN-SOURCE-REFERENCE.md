# Poetry in Motion: Open-Source and Public E-Commerce Projects

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Phase 1 technical intelligence (GitHub API and public documentation, May 2026)
Purpose: Map enterprise-grade and fashion-adjacent public codebases that Poetry in Motion can learn from, not blindly fork
Cross-reference: 04-technical-research/PROJECT-STRUCTURE.md, 01-global/INDUSTRY-ECOMMERCE.md, 05-critical-review/CRITICAL-REVIEW.md

Note: Star counts were fetched via GitHub API on 2026-05-27. Verify at the repository URL before making decisions.

---

## 1. Taxonomy

| Tier | Description | Typical licence |
|------|-------------|-----------------|
| A: Headless commerce core | Cart, catalog, orders, payments API | MIT, BSD, OSL |
| B: Enterprise monolith | Full store and admin in one codebase | OSL (Magento), GPL (WooCommerce) |
| C: ERP and apparel | Manufacturing, variants, BOM, inventory | GPL (ERPNext) |
| D: Storefront starters | Next.js and React frontends on Tier A | MIT |
| E: Open code (not OSS) | Source visible; production requires licence | Commercial |

---

## 2. Tier A: Headless Commerce (Primary References)

These are the closest public enterprise patterns for catalog, cart, checkout, and admin.

| Project | GitHub | Stars | Stack | Strengths | Limits for Poetry in Motion |
|---------|--------|-------|-------|-----------|------------------------------|
| Medusa | medusajs/medusa | Approximately 34,000 | Node/TypeScript, modular v2 | Modules, marketplace recipes, JS SDK, active community | No native style quiz; fashion requires custom modules |
| Saleor | saleor/saleor | Approximately 22,900 | Python, GraphQL | Multi-channel, multi-warehouse, mature OMS | Python stack if team is TypeScript-only |
| Spree | spree/spree | Approximately 15,400 | Ruby, Next starter | B2B, marketplace, multi-vendor (EE modules) | Ruby operations; EE required for advanced marketplace |
| Vendure | vendure-ecommerce/vendure | Approximately 8,200 | NestJS, GraphQL | Plugins, typed custom fields, admin UI | Smaller ecosystem than Medusa or Saleor |
| Sylius | sylius/sylius | Approximately 8,500 | PHP Symfony | BDD quality, REST, headless | PHP; approximately 2,500 live stores versus Magento scale |

Official storefronts and starters:

| Project | GitHub | Stars | Notes |
|---------|--------|-------|-------|
| Saleor Storefront | saleor/storefront | Approximately 1,400 | Next.js App Router, GraphQL |
| Medusa Next starter | medusajs/nextjs-starter-medusa | Approximately 2,800 | Pairs with Medusa backend |

Comparison sources: PkgPulse Medusa versus Saleor versus Vendure; OSSAlt Medusa versus Saleor.

---

## 3. Tier B: Enterprise Monolith and Mass Adoption

| Project | GitHub | Stars | Stack | Enterprise use | Fashion relevance |
|---------|--------|-------|-------|----------------|-------------------|
| Magento Open Source | magento/magento2 | Approximately 12,100 | PHP | Large catalogs, B2B EE, global brands | Apparel plugins, size and configurable products |
| WooCommerce | woocommerce/woocommerce | Approximately 10,300 | PHP WordPress | SMB scale, extensions | Fashion via themes and plugins |
| Solidus | solidusio/solidus | Approximately 5,300 | Ruby (Spree fork) | Maintained fork, API-first direction | Same as Spree lineage |

Commercial enterprise (not free OSS in production):

| Project | Model | Notes |
|---------|-------|-------|
| Adobe Commerce (Magento EE) | Licence 22,000 to 40,000+ USD per year | Qualimero TCO |
| Shopify Plus | SaaS | Not open source; de facto enterprise for DTC fashion |
| Spryker | Open code, not OSS | B2B and marketplace enterprise; evaluation-only licence |
| commercetools | Proprietary API-first | Often paired with custom fashion frontends |

---

## 4. Tier C: Fashion, Apparel, and Textile (ERP and Extensions)

Fashion operations including variants, BOM, and production often live in ERP, not in storefront repositories.

| Project | GitHub | Stars | Focus | What to borrow |
|---------|--------|-------|-------|----------------|
| ERPNext | frappe/erpnext | Approximately 35,000 | Full ERP | Item variants (size and colour), BOM, multi-warehouse |
| LS Shop | BuildWithHussain/ls_shop | Check repo | ERPNext e-commerce extension | SAC/SAV style attribute configurator, apparel POS |

Implementation guides: ClefinCode ERPNext textile.

Poetry in Motion: if creators become manufacturers, ERP patterns matter. If marketplace-only, Tier A headless is sufficient.

---

## 5. Tier D: Related Public Projects (Patterns, Not Full Commerce)

| Area | Examples | Use for research |
|------|----------|------------------|
| Search and discovery | Algolia integrations in Saleor and Medusa documentation | Faceted search for fashion attributes |
| PIM | akeneo/pim-community-dev | SKU, attributes, localisation at scale |
| Marketplace vendor | Spree EE multi-vendor, Medusa marketplace guides | Creator as vendor with split payouts |
| Payments Africa | Safaricom Daraja (not a fashion repository but a required integration) | M-Pesa STK Push |

---

## 6. Feature Matrix versus Poetry in Motion Prototype

| Capability | Medusa | Saleor | Spree | ERPNext and LS | Poetry in Motion (current) |
|------------|--------|--------|-------|----------------|----------------------------|
| Product catalog | Yes | Yes | Yes | Yes | Mock (3 SKUs) |
| Variants (size and colour) | Yes | Yes | Yes | Yes, SAC/SAV | Types only |
| Cart and checkout | Yes | Yes | Yes | Yes | Mock API |
| Multi-vendor | Recipes and custom | Apps | EE module | No | Creator mock |
| Subscriptions | Module | App | Extension | No | Mock route |
| Real payments | Plugins | Gateways | Stripe etc. | Gateways | No |
| Style quiz and AI | No, custom | No, custom | No, custom | No | UI only |
| Sustainability fields | Custom metadata | Metadata | Custom | Custom fields | Mock blocks |
| Trade-in and resale | Custom | Custom | Custom | No | Mock UI |

Conclusion: Poetry in Motion's differentiators (quiz, AI, circular, creator vote) are not solved by forking Medusa or Saleor alone. They require custom modules on top of a Tier A core, or continued custom Next.js with a real database.

---

## 7. Strategic Options

### Option 1: Stay Custom Next.js (Current Path)

| Pros | Cons |
|------|------|
| Full control of quiz, ethics UX, and brand | Must rebuild cart, payments, and tax |
| Matches existing v0 UI | 45 mock routes represent facade risk |

Mitigation: adopt Medusa or Saleor data models as reference; implement 8 core APIs only. See 05-critical-review/CRITICAL-REVIEW.md.

### Option 2: Medusa v2 as Commerce Backend

| Pros | Cons |
|------|------|
| TypeScript alignment; modules for marketplace | Learning curve; hosting overhead |
| Payment and shipping plugins | Fashion-specific logic still custom |

When to use: after wedge is locked and real checkout is needed.

### Option 3: Saleor plus Next Storefront

| Pros | Cons |
|------|------|
| Strong GraphQL, multi-warehouse | Python operations if team is Node-only |

When to use: large SKU count (50,000 or more). Not MVP.

### Option 4: ERPNext plus LS Shop

| Pros | Cons |
|------|------|
| Apparel variants plus manufacturing | Heavy; wrong if no factory |

When to use: creator-led production is core.

### Recommended for Poetry in Motion (Phase 2 Hypothesis)

Option 1 short-term plus Option 2 evaluation spike: a one-week Medusa proof of concept covering catalog, M-Pesa plugin research, and a single creator vendor. Do not adopt Magento or Spryker for MVP. TCO and team mismatch are prohibitive (Qualimero).

---

## 8. What to Study in Each Codebase

| Repository | Study these paths and concepts |
|------------|-------------------------------|
| medusajs/medusa | Module boundaries, cart workflows, promotion engine, marketplace recipe documentation |
| saleor/saleor | Channels, checkout, payment orchestration, metadata for sustainability |
| spree/spree | Multi-vendor order splitting (EE documentation), API v2 |
| saleor/storefront | Next.js App Router plus GraphQL patterns |
| BuildWithHussain/ls_shop | Style Attribute Configurator (SAC/SAV) for size and colour matrix |
| frappe/erpnext | Item variant model, BOM, stock ledger |

---

## 9. Contradictions and Limitations

| Issue | Detail |
|-------|--------|
| Stars do not equal production quality | WooCommerce stars are lower than Medusa but install base is far larger |
| Enterprise fashion is often closed | Zara and Shein stacks are proprietary |
| Open code is not free | Spryker and some Adobe modules require licences |
| Fashion OSS is sparse | Most repositories are general commerce; fashion means ERP variants |
| Fork maintenance cost | Upstream security patches are required |

---

## 10. Position in the Phase 1 Chain

```
INDUSTRY-ECOMMERCE.md and INDUSTRY-FASHION.md (business constraints)
        |
OPEN-SOURCE-REFERENCE.md (this document, technical options)
        |
PROJECT-STRUCTURE.md (current prototype map)
        |
CRITICAL-REVIEW.md (reject facade; pick wedge)
```

Action items:

- [ ] One-week spike: Medusa or bare Postgres. Document decision in 00-foundation/FOUNDATION.md.
- [ ] Copy SAC/SAV concept from LS Shop into Poetry in Motion product schema (size and colour as first-class).
- [ ] Remove unused API routes not present in reference platforms' MVP sets.

---

## 11. Source Bibliography

| Source | URL |
|--------|-----|
| GitHub API (star counts) | https://api.github.com/repos/{owner}/{repo} |
| Medusa repository | https://github.com/medusajs/medusa |
| Saleor repository | https://github.com/saleor/saleor |
| Spree repository | https://github.com/spree/spree |
| LS Shop | https://github.com/BuildWithHussain/ls_shop |
| ERPNext | https://github.com/frappe/erpnext |
| Sylius | https://github.com/sylius/sylius |
| Vendure | https://github.com/vendure-ecommerce/vendure |
| Qualimero platform comparison | https://qualimero.com/en/blog/ecommerce-platform-comparison |

Star snapshot (2026-05-27): Medusa approximately 33,981; Saleor approximately 22,923; Spree approximately 15,435; ERPNext approximately 35,011; Magento2 approximately 12,121; WooCommerce approximately 10,314; Vendure approximately 8,158; Sylius approximately 8,475; Solidus approximately 5,300.
