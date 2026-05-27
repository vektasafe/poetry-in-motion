# Research: Poetry in Motion

Author: James Kabingu, Vektasafe
Research model: Adapted from the Ganji Protocol. Structured as a pyramid: broad foundation at the base, narrowing through market and geographic layers, converging at the apex on a single MVP definition that initiates Phase 2 engineering.

---

## The Pyramid

```
                        [APEX]
                      06-mvp/
                    MVP.md
                  (Phase 2 start)
                /               \
           05-critical-review/
           CRITICAL-REVIEW.md
          (stress-test of all layers)
         /                         \
    04-technical-research/
    OPEN-SOURCE-REFERENCE.md
    PROJECT-STRUCTURE.md
   (prototype mapped to layers)
  /                               \
 03-market-intelligence/
 ENTITIES.md
 (named competitors, partners, infrastructure)
/                                             \
         02-africa/
         AFRICA.md  >  EAST-AFRICA.md  >  KENYA.md
         (continent to region to city)
        /                                         \
       01-global/
       LANDSCAPE.md
       INDUSTRY-ECOMMERCE.md
       INDUSTRY-FASHION.md
       (global history and industry data)
      /                                           \
     [BASE]
     00-foundation/
     FOUNDATION.md
     DATA-ETHICS.md
     (why this exists; what it refuses)
```

The base is the widest layer: philosophical foundation and historical context. Each layer above narrows the scope and increases specificity. The apex is the MVP definition, the narrowest and most actionable output. Every layer is load-bearing for every layer above it.

---

## Reading Order (Base to Apex)

Read in this sequence. Each document assumes the one before it.

| Step | Document | What it establishes |
|------|----------|---------------------|
| 1 | 00-foundation/FOUNDATION.md | The problem, the pillars, what Poetry in Motion refuses to copy |
| 2 | 00-foundation/DATA-ETHICS.md | Enforceable rules that apply to every layer above |
| 3 | 01-global/LANDSCAPE.md | Global industrial e-commerce and fashion history; what to inherit and what to reject |
| 4 | 01-global/INDUSTRY-ECOMMERCE.md | Global e-commerce market size, business models, take rates |
| 5 | 01-global/INDUSTRY-FASHION.md | Global fashion industry economics, resale, circular, AI |
| 6 | 02-africa/AFRICA.md | Continental Africa e-commerce and fashion context; structural enablers and barriers |
| 7 | 02-africa/EAST-AFRICA.md | EAC regional context: logistics, payments, creator ecosystem, regulatory |
| 8 | 02-africa/KENYA.md | Kenya-specific market, payments, logistics, regulation, and creator landscape |
| 9 | 03-market-intelligence/ENTITIES.md | Named competitors, partners, infrastructure providers, and regulators |
| 10 | 04-technical-research/OPEN-SOURCE-REFERENCE.md | Public commerce codebases: what to learn, what to avoid |
| 11 | 04-technical-research/PROJECT-STRUCTURE.md | Current prototype mapped to five-layer architecture |
| 12 | 05-critical-review/CRITICAL-REVIEW.md | Contradictions, failures, and P0 actions before public launch |
| 13 | 06-mvp/MVP.md | The wedge decision. Phase 2 starts here. |

---

## Phase Status

### Phase 1 (current): Research foundation

All documents in steps 1 through 13 above constitute Phase 1. Phase 1 is complete when the Phase 1 exit checklist in 06-mvp/MVP.md is fully checked.

### Phase 2 (next): Engineering MVP

Phase 2 begins after all P0 items in 05-critical-review/CRITICAL-REVIEW.md are resolved and the wedge in 06-mvp/MVP.md is confirmed. Engineering scope is defined in 06-mvp/MVP.md.

### Phase 3 (planned): Deep dives and real recommendations

| Topic | Planned document |
|-------|-----------------|
| AI styling ethics and bias | 04-technical-research/ |
| Supply chain verification | 03-market-intelligence/ |
| East Africa retail primary research | 02-africa/ |
| Kenya and EAC regulatory compliance | 02-africa/KENYA.md extension |

### Phase 4 (planned): Production architecture

Compliance, monitoring, legal, and production SLAs. Documented when Phase 3 is complete.

---

## Rules of Use

1. Do not treat mock APIs as production claims until tags move from [IMPLEMENTED] to [VALIDATED] against real data.
2. Add new research under the numbered folders, not the repository root.
3. Align code changes with 01-global/LANDSCAPE.md Part 3.2 (inherit and reject table) before expanding scope.
4. Any strategy change must be reflected in 06-mvp/MVP.md before the corresponding code is written.
5. CRITICAL-REVIEW.md is reviewed quarterly. It takes precedence over foundation documents where they conflict.

---

## Legacy Notes

The previous folder structure (01-foundation/, 02-market-intelligence/, 03-technical-research/) has been superseded by the pyramid structure above. All content has been carried forward and reorganised. No research has been discarded.
