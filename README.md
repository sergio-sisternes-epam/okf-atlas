# okf-atlas

Dedicated Atlas store for the okf skill. This is a **store package**, not a skill — there is no `SKILL.md`.

OKF root is the **git root** (`SCHEMA.json` next to this README), not a nested `atlas/` folder. Git root also holds package metadata (`README.md`, `apm.yml`, `.gitignore`, optional `LICENSE`).

Consumers mount this repo, then point `--root` at the **clone root** (not `…/atlas`):

```text
atlas auth login --host github.com
atlas mount github.com/sergio-sisternes-epam/okf-atlas --ref main
atlas compile --root .atlas/github.com/sergio-sisternes-epam/okf-atlas
atlas search "…" --root .atlas/github.com/sergio-sisternes-epam/okf-atlas
```

Default clone path: `.atlas/github.com/sergio-sisternes-epam/okf-atlas`

Compile/query root: `.atlas/github.com/sergio-sisternes-epam/okf-atlas` (the clone root)

APM dependencies: `sergio-sisternes-epam/okf`, `sergio-sisternes-epam/atlas`.
