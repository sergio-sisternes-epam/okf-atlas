---
type: experience
title: "Implement review-package recommended_changes: substrate contract + outdated name + SCHEMA frontmatter on okf"
description: "Applied approved plan from review-package: portable multi-harness substrate contract wording in SKILL.md, okf-export, okf-import; fixed wiki→okf-wiki; added type to SCHEMA.md"
created: 2026-08-18
work_id: okf-review-package-2026-08-18
status: raw
origin: internal
sensitivity: internal
relates_to:
  - path: work/okf-review-package-2026-08-18.md
    kind: implements
---

# Implement review-package recommended_changes on okf

## Enter (this Run)

```text
mode: run
subject: okf
path: implement
path_module: references/paths/implement.md
intent: implement the approved review-package recommended_changes (substrate-contract wording + outdated name fix; optional SCHEMA frontmatter)
```

## Approved plan (pinned from prior review-package REPORT)

1. Replace every abbreviated “load X” / “hand off to X” claim that targets another skill or progressive module with the portable three-step substrate contract. Apply to:
   - SKILL.md (okf-authority and okf-wiki hand-offs)
   - references/modules/okf-export.md
   - references/modules/okf-import.md
2. Fix outdated “wiki” → “okf-wiki” in okf-import.md (and export).
3. (Optional soft) Add minimal frontmatter to SCHEMA.md (type: schema).

## What was done

- Updated `SKILL.md` “How to route” section + added full Substrate contract section.
- Updated `references/modules/okf-export.md`: Rules + Substrate contract; softened absolute paths in Process to path-resilient wording; fixed load language.
- Updated `references/modules/okf-import.md`: Rules + Substrate contract; fixed “wiki” → “okf-wiki”.
- Added YAML frontmatter (`type: schema`) to `references/wiki/SCHEMA.md`.

No other product files touched. No knowledge pages under `knowledge/` created or materially updated.

## Durable conclusions / ingest

No durable knowledge-page promotion claimed in this Run. Findings already captured in the prior advisory review experience.  
**ingest: defer** — advisory wording fixes only; no new procedures or ontology changes to promote.

## Related

- [[raw/experiences/2026-08-18-review-package-okf]] — the advisory review that produced the approved plan
- Autogenesis path implement (subject = okf)

## Changed files

- SKILL.md
- references/modules/okf-export.md
- references/modules/okf-import.md
- references/wiki/SCHEMA.md
- references/wiki/raw/experiences/2026-08-18-implement-substrate-contract-okf.md (this file)
