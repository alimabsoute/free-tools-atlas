# The Contraband Atlas

**A beautiful, audited catalog of 100 genuinely useful free tools — plus an executive summary and 20 product ideas built on top of them.**

🔗 **Live:** https://alimabsoute.github.io/free-tools-atlas/

---

## What's inside

| Page | What it does |
|------|--------------|
| **[Catalog](index.html)** | All 100 free tools across 12 categories, with honest reviews, live search/filter, and freemium / ⚠️ grey-area flags. |
| **[Executive Summary](summary.html)** | The highest-leverage tools, ranked — then mapped directly to a real project stack (content, SEO, frontend, dev, research, security). |
| **[20 Ideas](ideas.html)** | Twenty novel products you could build by combining these tools, each tagged with its stack, fit, and monetization angle. |

## Sources & method

Built on the **[websites-100-audit](https://github.com/Moh4696/websites-100-audit)** repository — 100 free tools, each with an honest one-line review and a full HTTP liveness audit (98/100 live). Capabilities reflect that curated audit rather than a fresh crawl of every site; the audit had already verified each link, so a re-crawl would add cost without new signal.

Audit corrections carried in: `annas-archive.org` → `annas-archive.gs` (old domain dead), `ray.so` → `www.ray.so` (apex refuses HTTPS), Fakespot retired → TheReviewIndex.

> ⚠️ Four entries (pdfdrive, libgen, anna's archive, sci-hub) are flagged grey-area piracy and included only for completeness, exactly as flagged in the source audit.

## Design

A refined editorial-almanac aesthetic with a subtle classified-dossier motif — warm paper, ink, a single stamp-red accent, Fraunces / Schibsted Grotesk / JetBrains Mono. Full design contract in **[DESIGN.md](DESIGN.md)**. Mobile-first, fully static, no build step.

## Run locally

Just open `index.html` in a browser — no dependencies, no build.
