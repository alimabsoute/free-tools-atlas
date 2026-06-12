# CLAUDE.md — The Contraband Atlas (free-tools-atlas)

<!-- push-tier: 2 -->
<!-- 1 = deploy-wired: NEVER push (CLI deploy only). 2 = public: push only after secret scan. 3 = private non-deploy: auto-commit + auto-push OK -->

> **Folder → repo:** local `free-tools-atlas/` → GitHub `alimabsoute/free-tools-atlas`. Live: **https://alimabsoute.github.io/free-tools-atlas/** (GitHub Pages).

## What this is
A static, audited catalog of 100 genuinely useful free tools, plus an executive summary and 20 product ideas built on top of them.

## Stack
Pure **static HTML** — no build step, no dependencies. Hosted on GitHub Pages (served from repo root).

## Files
- `index.html` — the 100-tool catalog (main page)
- `summary.html` — executive summary
- `ideas.html` — 20 product ideas
- `DESIGN.md` — design system / visual spec
- `logs/` — harness artifacts (gitignore-worthy; don't stage)

## Deploy
Push to `main` → GitHub Pages serves it automatically. No CLI build.
```bash
git add index.html summary.html ideas.html DESIGN.md README.md   # stage by name, not -A
git commit -m "..." && git push
```

## Gotchas
- ⚠️ Never `git add -A` here — the harness drops `logs/permission_request.json` (can contain command text) into the repo. Stage files by name; run `git ls-files` before any push (this is a public Pages repo).
- No secrets belong in this repo — it's public.
