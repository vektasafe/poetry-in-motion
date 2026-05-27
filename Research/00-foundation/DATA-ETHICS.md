# Poetry in Motion: Data Ethics

Authors: Silvester Ndaigiri and James Kabingu, Vektasafe
Status: Draft, enforceable rules for P0 before public users
Cross-reference: 05-critical-review/CRITICAL-REVIEW.md, section 6.5

---

## 1. Scope

This document applies to: the style quiz, profile fields (body type, skin tone, budget, occasions), uploaded images, order and payment metadata, and creator KYC in future phases.

---

## 2. Principles

1. Collect minimum. Only fields that change recommendations or fulfillment in the current release are collected.
2. Explain at collection. One plain-language sentence per sensitive field states why it is asked.
3. Opt out. A "prefer not to say" option must exclude the field from models entirely. It must not store null as a category.
4. No false precision. Demo AI must be labelled. No confidence scores appear in production until they are calibrated against real outcomes.
5. No sale of personal data. No third-party ad targeting from style profiles.
6. Retention limits. Profile data is deleted on account deletion within 30 days. This is a target for Phase 2 database implementation.
7. Images. Uploads are used only for the stated purpose. They are deleted or anonymised after analysis unless the user explicitly saves them to their profile.

---

## 3. Sensitive Attributes

| Field | Risk | Rule |
|-------|------|------|
| Body type | Stereotyping, exclusion | Not used as sole ranking signal. Free-text fit notes are added in Phase 2. |
| Skin tone | Colorism in recommendations | Human-reviewed palette rules are required before automating colour suggestions. |
| Photos | Biometric adjacent | Explicit consent checkbox required. No training on user photos without a separate opt-in. |

---

## 4. Sustainability Data

No CO2, water, or verified labels appear on SKUs without a sustainability_source_id in the database pointing to an auditable record. UI copy when the source is missing: "Impact data not yet verified for this item."

---

## 5. Public Demo Rules

DEMO_MODE deployments: no real payments, a visible banner indicating demo status, and synthetic metrics hidden from the UI.

---

## 6. Review Triggers

This document is revisited when any of the following occur: minors are added as a user segment, EU users are targeted, automated profiling is introduced, or Kenya Data Protection Act or GDPR-equivalent rights obligations change.
