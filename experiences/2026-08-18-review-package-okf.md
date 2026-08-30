---
type: experience
title: "Autogenesis review-package of okf skill for multi-harness nesting contract conformance"
description: "Advisory audit of okf package against the skill-nesting substrate contract; gaps found in load/hand-off wording"
created: 2026-08-18
work_id: okf-review-package-2026-08-18
status: raw
source: runtime-aware
origin: internal
sensitivity: internal
relates_to:
  - path: work/okf-review-package-2026-08-18.md
    kind: implements
---

# Autogenesis review-package of okf

## User ask

autogenesis skill review okf skill and confirm the package is conformant

## Enter

mode: run
subject: okf
path: review-package
path_module: references/paths/review-package.md
intent: review okf skill and confirm the package is conformant

## What was done

1. Loaded nesting knowledge page skill-nesting-invocation-pattern.md from autogenesis wiki.
2. Identified target: /home/workdir/.grok/skills/okf/
3. Examined SKILL.md and the three modules under references/modules/ (okf-authority, okf-export, okf-import).
4. Searched for every skill-to-skill or module load / hand-off claim.
5. Compared against the portable substrate contract (locate by name → load full body with on-demand loader → follow exactly → re-execute live tools).
6. Produced the structured REVIEW-PACKAGE REPORT (see below).
7. No mutation of okf skill bodies (advisory only). Subject wiki was missing; skeleton initialised under okf/references/wiki/ solely to satisfy Exit lineage root requirement.

## REVIEW-PACKAGE REPORT

target: /home/workdir/.grok/skills/okf/
substrate_contract: gaps
harness_mapping: n/a
gaps:
  - SKILL.md:31 — "load `okf-authority`." lacks the three-step substrate contract
  - SKILL.md:33 — "**hand off to `okf-wiki`**." lacks the three-step substrate contract (locate by name, load full SKILL.md body, follow exactly)
  - references/modules/okf-export.md:29 — "Always load the `okf-authority` module (or the parent `okf` skill)" lacks substrate contract
  - references/modules/okf-import.md:27 — same "Always load the `okf-authority` module..." lacks substrate contract
  - references/modules/okf-import.md:28 — "Use the `wiki` skill for all writes" (outdated name; should be okf-wiki) and lacks substrate contract
  - references/modules/okf-export.md:12,16 — absolute paths to session wiki and artifacts (not a nesting violation, but path-resilient wording preferred for portability)
suggested_fix: |
  Replace every "load X" / "hand off to X" claim that targets another skill or progressive module with the portable substrate contract text:

  When this body must invoke / load / execute another skill (or its module):
  1. Locate the target skill by name from the harness’s available skills list (do not hard-code absolute paths).
  2. Load the full body of that skill’s entrypoint (SKILL.md) using the harness’s on-demand skill-loader tool. Never rely on the short frontmatter description alone.
  3. Follow the loaded body instructions exactly.
  4. Re-execute any live tool calls the body requires.

  For internal progressive-disclosure modules under references/modules/, the same pattern applies by reading the module file after locating the parent skill, or an explicit "read_file the module path relative to the loaded skill root".
status: needs-work

## Durable conclusions claimed?

No product changes. The report itself is advisory. Explicit defer of wiki-ingest: the findings are a one-time audit snapshot, not yet promoted to lasting rules for the okf package. Future implement path (if operator approves) would turn the suggested_fix into actual wording changes.

## Related

- [[knowledge/skill-nesting-invocation-pattern]] (from autogenesis wiki; source of the contract under review)
- Autogenesis path review-package

## Changed files

- references/wiki/ (skeleton created: SCHEMA.md, index.md, log.md, quality-config.json, raw/, knowledge/, modules/, sources/, log/)
- raw/experiences/2026-08-18-review-package-okf.md (this file)

No SKILL.md or module bodies were edited.
