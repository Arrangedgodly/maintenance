# Context

Glossary for the home-improvement publishing project. Canonical definitions only — no implementation detail, no specs. Terms are captured as they are resolved in design conversations.

---

## Quartz v5
Jacky Zhao's static-site generator. A Node project (`package.json`, `quartz/`, `quartz.config.ts`, `quartz.layout.ts`) that turns a folder of Markdown into a static HTML site. You run `npx quartz build` to produce `public/`. This project's **renderer** layer.

## Quartz Syncer
An Obsidian community plugin. Pushes Markdown from a vault folder to a GitHub repo using a personal access token (PAT). Does **not** build anything — transport only. This project's **transport** layer. Distinct from Quartz v5 despite the shared name.

## content/
The folder Quartz v5 treats as publishable input. In this project, the publishable content is the vault's `reference/` folder (notes + GLOSSARY.md + the HVAC reference doc). Quartz's `configuration.content` is pointed at it. The transport layer (Syncer) writes into this folder; the renderer (Quartz v5) reads from it.

## transport
Getting Markdown from the Obsidian vault into the GitHub repo. Quartz Syncer's job. One of the two layers required for a note change to appear on the public site.

## build / deploy
Running `npx quartz build` to produce static HTML and uploading it to GitHub Pages. Done by the `deploy.yml` GitHub Action on every push. The other of the two layers. Distinct from transport — a note can be transported but not yet built, or built but not yet deployed.

## deploy.yml
The Quartz-canonical GitHub Actions workflow (`/.github/workflows/deploy.yml`) that checks out the repo, runs `npx quartz build`, and uploads the `public/` output to GitHub Pages. Triggers on push to the default branch.

## baseUrl
A Quartz config value (`configuration.baseUrl` in `quartz.config.ts`) that sets the URL subpath the site is served from. Empty string `""` for a root/custom-domain deployment (this project's choice); `"/<repo>/"` for a `user.github.io/<repo>` project site. Baked into every generated link — getting it wrong breaks all CSS and internal links.

## Pages Source
A setting under the repo's Settings → Pages: where GitHub finds the HTML to serve. For this project, set to "GitHub Actions" (not "Deploy from a branch"), so the `deploy.yml` Action is the deploy mechanism.

## custom domain (GitHub Pages)
A public hostname (here: `maintenance.graydonwasil.com`) pointed at GitHub Pages via DNS records at the domain provider. Set in Settings → Pages → Custom domain. GitHub provisions a Let's Encrypt TLS cert after DNS propagates. Requires `baseUrl: ""` in Quartz config.

## light/dark theme
Quartz v5's default dual theme, driven by CSS custom properties. `theme.colors.light` and `theme.colors.dark` in `quartz.config.ts` define each variant; the site follows the visitor's OS preference and provides a toggle. This project ships both.

## theme variables
The CSS custom properties (`background`, `primary`, `secondary`, `light`, `tertiary`, `darkmode` color sets, plus `typography.header`/`body`/`code` fonts) exposed in `quartz.config.ts` under `theme`. The system every Quartz theme — built-in or community — is constructed from. The foundation for any styling work.

## publishable / private
The security boundary for this vault. `reference/` is publishable (goes to `content/`, becomes public). Everything else — `ACTION-ITEMS.md`, `NOTES.md` (contains equipment serials), `learning-records/`, `lessons/`, `.obsidian/` — is private and never leaves the machine. `ACTION-ITEMS.md` gets a public stub so `[[ACTION-ITEMS]]` links resolve on the site without leaking the real list.
