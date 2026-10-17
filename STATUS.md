# STATUS — antiapps (2026-10-17)

## What this is
Master static landing for the **anti family** (GitHub Pages, branch `main`, site root). No workflows. Hosts pages for antiHunt, antiDrive, antiBot, antiQA, etc. Mirror: `antiloki/antiapps`.

## Context
## Shared context (Dan / anti family)
- Stack rule: **Rust + Tauri + SQLite** in product code. TypeScript only where clearly better (Tauri FE, Cloudflare Workers, Remotion offline assets).
- Heavy jobs (cargo/tauri builds, E2E, ffmpeg) go through **jobq** on the shared box. Stop if free disk is under 10 GB.
- No GitHub Actions (no CI credits). Build/test/release locally; `gh release create` for uploads.
- Merge once local tests pass; Dan does not review PRs. Never force-push. Never delete without Dan's yes.
- Products are named **anti + the problem** (antiHunt, antiDrive, antiBot, antiQA, Antiloki…). Public copy: local, one-time or free, private. Never mention Linear in public copy.

- antiHunt EN marketing lives here; minemylead.com is the separate PT funnel.

## Done
- antiDrive site updates through 0.1.11 (downloads + local AI tour clip).
- antiHunt pages listing recent client versions; `/trial` free-trial page (Turnstile-ready, closed until API set) + privacy-friendly analytics (no cookies/IPs) on branch `ah-trial-page`.
- Palette mockups / per-app colours work on side branches.

## Missing / next
- Point `/antihunt/trial/` at the live order-server API when deployed.
- Merge or publish outstanding trial/notes branches (`ah-trial-page`, version note pages) as needed.
- Keep download links aligned with latest `gh release` assets from MineMyLead-app / antiDrive packs.

## Build & run
Static HTML/CSS/JS. Serve the repo root (e.g. `python3 -m http.server`) or push to `main` for GitHub Pages. No build step required for most pages.
