# ADR 0001: Quartz Syncer for transport, GitHub Action for build/deploy

- **Status:** proposed
- **Date:** 2026-07-28

## Context

Publishing the `reference/` notes to a public Quartz v5 site requires two distinct things to happen for each edit:

1. **Transport** — the new Markdown travels from the Obsidian vault into the GitHub repo.
2. **Build/deploy** — Quartz v5 runs `npx quartz build` and the resulting `public/` HTML is served by GitHub Pages.

The author has prior experience with the Quartz Syncer Obsidian plugin (DNS records, GitHub PAT) and wants the "publish from inside Obsidian" workflow. Alternatives considered:

- **`git push` from a terminal + Action** — one tool, one token, no plugin. Simpler and more robust; loses the in-Obsidian publish button. Author would still be in a terminal frequently for theming work.
- **Local build + push built HTML** — fights Syncer's design (it syncs vault content, not arbitrary build output). Rejected.
- **Cloud-only Quartz (no local install)** — incompatible with the stated goal of learning theming, which requires local preview.

## Decision

Use **Quartz Syncer** for transport (commits Markdown from Obsidian into `content/` via a fine-grained PAT with `contents: write`) and the **Quartz-canonical `deploy.yml` GitHub Action** for build/deploy (`npx quartz build` → upload to Pages, on every push).

The Quartz v5 framework lives in the vault root (the vault IS the Quartz repo). The cloned Quartz repo's `.git` is discarded so the vault's own git history adopts the framework files. `content/` is a **symlink to `reference/`** (created via `npx quartz create --strategy symlink --source reference/`), so there is a single copy of the notes on disk: edits happen in `reference/` inside Obsidian, Quartz reads them through the symlink, and local preview (`npx quartz build --serve`) sees the same files.

Note (v5 specifics discovered during scaffold): Quartz v5 uses **`quartz.config.yaml`** for config (not the v4 `quartz.config.ts`); `baseUrl`, theme, and plugin options all live there.

## Consequences

- **Two configs to manage:** the Syncer PAT, and the Pages Source setting ("GitHub Actions"). DNS is set once for the custom domain.
- **One additional failure surface:** the Syncer plugin can break on Obsidian updates or if GitHub changes PAT scope rules. Mitigated by the plugin's popularity and the fallback of a direct `git push`.
- **Local Node required** for theming/preview, but not for routine publishing (the Action builds remotely).
- **Single copy of notes on disk** — Obsidian edits and Quartz preview read the same files, no drift.
