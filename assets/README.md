# `assets/`

- **`accounting/`** — Desktop installers for **The Abacus Accounting** (staged for release tags such as `v4.0.1`). Do not edit binaries in production; [The-Abacus-Accounting-Web](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Web) CI can sync into this tree.
- **`pdf/`** — Desktop installers for **The Abacus PDF** (e.g. `0.4.0` in filenames). The PDF app pipeline syncs into this folder. See `pdf/README.md`.

Version numbers appear in the **file names**; we do not use a nested `v1.2.3/` subfolder for Accounting or `latest/` / `v0.x/` subfolders for PDF in this layout.
