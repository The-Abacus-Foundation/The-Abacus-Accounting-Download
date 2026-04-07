# The-Abacus-Accounting-Download

Desktop installers for **The Abacus Accounting** (macOS, Windows, Linux).

## Download the installers

Binaries are **not** in the repository root. They live under **`assets/v{version}/`**.

| Where | Link |
|--------|------|
| **GitHub Release** (recommended) | [**Latest release**](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Download/releases/latest) — attached `.dmg`, `.msi`, `.AppImage` |
| **Browse in repo** | [**`assets/v4.0.1/`**](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Download/tree/main/assets/v4.0.1) — same files committed to `main` (version folder matches `release-assets.json`) |

On the GitHub **Code** tab, open the **`assets`** folder, then the version folder (e.g. **`v4.0.1`**), to see the three installer files.

## How files get here

On each successful [Desktop installers](https://github.com/The-Abacus-Foundation/The-Abacus-Accounting-Web/actions/workflows/desktop-build.yml) workflow run on **The-Abacus-Accounting-Web**, CI:

1. Copies the three staged installers into **`assets/v{version}/`** (version from `web/package.json` in the main repo).
2. Updates **`release-assets.json`** with filenames and tag.
3. Pushes to **`main`** on this repository (requires the **`DOWNLOAD_REPO_TOKEN`** secret on the web repo).
4. Uploads the same files to a **GitHub Release** `v{version}` — these URLs are what **accounting.theabacus.org** links to.

## Layout

- **`assets/v4.0.1/`** (example) — versioned installer binaries.
- **`release-assets.json`** — manifest for tooling; filenames include the app version (e.g. `abacus-accounting-macos-arm64-4.0.1.dmg`).
