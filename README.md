# okf-atlas

Dedicated Atlas store for the okf skill. This is a **store package**, not a skill — there is no `SKILL.md`.

OKF root is `atlas/` (`atlas/SCHEMA.json`), not the git root. Git root holds only package metadata (`README.md`, `apm.yml`, `.gitignore`, optional `LICENSE`).

Consumers mount this repo, then pass `--root` at the nested `atlas/` directory:

```text
atlas auth login --host github.com
atlas mount github.com/sergio-sisternes-epam/okf-atlas --ref main
atlas compile --root .atlas/github.com/sergio-sisternes-epam/okf-atlas/atlas
atlas search "…" --root .atlas/github.com/sergio-sisternes-epam/okf-atlas/atlas
```

Default clone path: `.atlas/github.com/sergio-sisternes-epam/okf-atlas`
Compile/query root: `.atlas/github.com/sergio-sisternes-epam/okf-atlas/atlas`

APM dependencies: `sergio-sisternes-epam/okf`, `sergio-sisternes-epam/atlas`.
