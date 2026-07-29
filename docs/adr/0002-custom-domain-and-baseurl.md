# ADR 0002: Custom domain (`maintenance.graydonwasil.com`) with `baseUrl: ""`

- **Status:** proposed
- **Date:** 2026-07-28

## Context

The site needs a public URL. Three options:

1. `<user>.github.io` root — repo must be named `<user>.github.io`. `baseUrl: ""`. No DNS unless a custom domain is layered on top.
2. `<user>.github.io/<repo>` project site — any repo name, no DNS, but every URL is prefixed with `/<repo>/`. Requires `baseUrl: "/<repo>/"`.
3. **Custom domain** — works with any repo name. DNS records at the provider point a hostname at GitHub Pages; Pages provisions TLS via Let's Encrypt. `baseUrl: ""`.

The author has done the DNS-record step before, has a personal domain (`graydonwasil.com`), and wants a clean URL for a subdomain (`maintenance.graydonwasil.com`).

`baseUrl` is baked into the build output: every generated link and asset reference depends on it. Switching from a `/<repo>/` project path to a custom domain (or vice versa) means reconfiguring Quartz, re-running the Action, and — if DNS is involved — waiting for propagation. DNS propagation is the only slow step in the whole publish workflow.

## Decision

Use the **custom domain `maintenance.graydonwasil.com`** with **`baseUrl: maintenance.graydonwasil.com`** (bare hostname, no protocol, no trailing slash) in `quartz.config.yaml`. The repo can be named anything (e.g. `home-improvement`); GitHub Pages is configured with the custom domain, and DNS at the provider points the subdomain at Pages.

Note (v5 specifics): Quartz v5's `baseUrl` is the **bare hostname** for a root-served custom domain — *not* an empty string. Quartz uses it to build absolute URLs for sitemap, RSS, and Open Graph image tags, so it must be a real hostname. For a `user.github.io/<repo>` project site it would be `user.github.io/repo`. The CLI's `create` prompt intentionally rejects empty values.

## Consequences

- **Cleanest URLs:** `maintenance.graydonwasil.com/HVAC-Filter-Change` (no `/repo/` subpath).
- **Simple config:** `baseUrl` is the bare hostname.
- **DNS step is required** and is the slow step: CNAME (or A records) at the provider, then wait for propagation before GitHub issues the TLS cert. Sequence this before expecting the site to resolve.
- **One-time DNS, then forget it:** once the record is in place and Pages has the cert, subsequent publishes need no DNS interaction.
