# okf-atlas

Plain Atlas store for OKF process memory.

The Atlas store root is the **git root**, where `SCHEMA.json` and `index.md`
live. It is not a nested `atlas/` directory.

## Mount

Mount this repository with Atlas, then use the resolved clone root for compile
and search operations:

```text
atlas auth login --host github.com
atlas mount github.com/sergio-sisternes-epam/okf-atlas --ref main
atlas resolve github.com/sergio-sisternes-epam/okf-atlas
atlas compile --root .atlas/github.com/sergio-sisternes-epam/okf-atlas
atlas search "…" --root .atlas/github.com/sergio-sisternes-epam/okf-atlas
```

The default mount, compile, and search root is
`.atlas/github.com/sergio-sisternes-epam/okf-atlas`.

From this repository, compile the store directly at the git root:

```text
atlas compile --root .
atlas search "…" --root .
```

## ALL RIGHTS RESERVED

Copyright (c) 2026 Sergio Sisternes. All rights reserved.

See [LICENSE](LICENSE). Public visibility does not grant permission to use,
copy, modify, or distribute this repository.
