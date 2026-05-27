# Contributing to Poetry in Motion Research

Author: James Kabingu, Vektasafe
Last updated: June 2026

---

## Purpose

This document governs how new research is added to this repository. The research is structured as a pyramid with a mandatory reading order. A document added without following this structure degrades the pyramid into a folder of notes.

---

## Before Adding a New Document

Answer these three questions before writing anything.

1. Which existing document does this new document depend on? Name it explicitly.
2. Which existing document does this new document inform or feed into? Name it explicitly.
3. Does it belong in an existing numbered folder, or does it require a new layer?

If you cannot answer questions 1 and 2, the document is not ready to be written.

---

## Folder Rules

| Folder | What belongs here |
|--------|------------------|
| 00-foundation/ | Why Poetry in Motion exists. Ethical constraints. These change rarely. |
| 01-global/ | Global e-commerce and fashion history and industry data. |
| 02-africa/ | Africa, East Africa, and Kenya market intelligence. Geographic narrowing only. |
| 03-market-intelligence/ | Named entities: competitors, partners, infrastructure, unit economics. |
| 04-technical-research/ | Prototype structure, open-source references, technical options. |
| 05-critical-review/ | Stress-test of all layers. Lives locally only. Not pushed to GitHub. |
| 06-mvp/ | The wedge decision and Phase 2 gate. One document. |

Do not add documents to the repository root. Do not create new numbered folders without updating the README reading order table.

---

## PR Checklist

Every pull request that adds or modifies a research document must confirm the following.

- [ ] The document states its cross-references at the top (which documents it depends on and which it informs).
- [ ] The document is placed in the correct numbered folder.
- [ ] The README reading order table has been updated if a new document was added.
- [ ] No claim is made without a source citation or a notation of [ASSUMED], [HYPOTHESIS], or [RESEARCH DIRECTION].
- [ ] No CO2, water, or verified sustainability label is introduced without a sustainabilitySourceId reference.
- [ ] No AI confidence score is introduced without a calibration methodology.
- [ ] If the document touches the reject list in 01-global/LANDSCAPE.md Part 3.2, the corresponding acceptance criterion has been checked or updated.
- [ ] Writing style follows technical research standards: no em dashes, no rhetorical questions, no bold for emphasis in prose.

---

## Notation Standards

Use these tags consistently across all documents.

| Tag | Meaning |
|-----|---------|
| [VALIDATED] | Verified in the repository. File exists and route responds in development. |
| [IMPLEMENTED] | Present as prototype or mock. Not production-hardened. |
| [HYPOTHESIS] | Design intent not yet built. |
| [RESEARCH DIRECTION] | Identified for a later phase. |
| [KNOWN] | Sourced from confirmed or reported research. |
| [ASSUMED] | Reasonable estimate pending Phase 2 validation. |
| [UNKNOWN] | Must be measured from real transactions or primary research. |
| [MEASURED] | Validated against real data. Replace [ASSUMED] or [UNKNOWN] when data arrives. |
| [CONFIRMED] | Sourced from a primary source (SEC filing, official documentation). |
| [REPORTED] | Sourced from press or analyst coverage. Treat as directional. |
| [INFERRED] | Derived from entity behaviour or indirect evidence. |

---

## What Not to Do

- Do not add a document that duplicates content already in an existing layer. Extend the existing document instead.
- Do not add market data without noting the definition used (retail B2C only versus total digital economy).
- Do not add entity profiles to 01-global/ or 02-africa/. Entity profiles belong in 03-market-intelligence/ENTITIES.md.
- Do not modify 06-mvp/MVP.md without the sign-off field being re-confirmed by the founder.
- Do not push 05-critical-review/ to GitHub. It is in .gitignore for a reason.
