# The Abacus — App download repository

This repo hosts the **GitHub-mirrored desktop installers** for The Abacus Foundation’s browser apps. Binaries are **not** in the repository root: they sit under `assets/`.

| App | Web app | Installers in this repo |
|-----|---------|-------------------------|
| **The Abacus Accounting** | [accounting.theabacus.org](https://accounting.theabacus.org) | [`assets/accounting/`](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/tree/main/assets/accounting) — `.dmg`, `.msi`, `.AppImage` (version in filenames) |
| **The Abacus PDF** | [pdf.theabacus.org](https://pdf.theabacus.org) | [`assets/pdf/`](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/tree/main/assets/pdf) — `.dmg`, `.msi`, `.AppImage` (version in filenames) |

## Download from GitHub

| | Accounting | PDF |
|---|------------|-----|
| **Release (recommended)** | [**Latest / tagged releases**](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/releases) — use tag **`v4.0.1`** (or current tag) for Accounting assets | Same [releases](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/releases) — use tag **`v0.4.0`** (or current tag) for PDF assets |
| **Browse `main`** | [Folder `assets/accounting/`](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/tree/main/assets/accounting) | [Folder `assets/pdf/`](https://github.com/The-Abacus-Foundation/The-Abacus-App-Download/tree/main/assets/pdf) (installers next to that folder’s `README.md`) |

On the **Code** tab, open **`assets`**, then **`accounting`** or **`pdf`**, to see the three platform files for each app.

## How files get here

- **Accounting** — On each successful [Desktop installers](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Web/actions/workflows/desktop-build.yml) run on [The-Abacus-Accounting-Web](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Web), CI can sync builds into **`assets/accounting/`**, update **`release-assets.json`**, and publish a **GitHub Release** `v{version}`. The **`DOWNLOAD_REPO_TOKEN`** secret (on the web repo) must allow push to this repository.
- **PDF** — The PDF desktop workflow syncs builds into **`assets/pdf/`** and updates **`assets/pdf/release-assets.json`**.

> **CI paths:** Pipelines that still reference `assets/v{version}/` or `assets/pdf/latest/` should be updated to target **`assets/accounting/`** and a **flat** **`assets/pdf/`** (no `latest/`, no per-version subfolders in-repo).

## Layout (this repository)

- **`assets/accounting/`** — The Abacus Accounting desktop installers; see [`assets/accounting/README.md`](assets/accounting/README.md), manifest: [`release-assets.json`](release-assets.json).
- **`assets/pdf/`** — The Abacus PDF desktop installers; see [`assets/pdf/README.md`](assets/pdf/README.md), manifest: [`assets/pdf/release-assets.json`](assets/pdf/release-assets.json).

## Repository

**https://github.com/The-Abacus-Foundation/The-Abacus-App-Download**

(Older docs may refer to the repository name *The-Abacus-Accounting-Download*; this repo is the unified app-download mirror.)
