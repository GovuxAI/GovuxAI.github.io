# GovuxAI.github.io

Static landing page for [Govux](https://github.com/GovuxAI/govux) — AI-powered UX governance for frontend teams.

Hosted at **https://GovuxAI.github.io** via GitHub Pages.

## What's on the page

| Section | Description |
|---------|-------------|
| Hero | One-liner pitch + live code snippet showing the PR check run output |
| How it works | 4-step flow: webhook → AST+LLM → score → GitHub Check Run |
| Features | 6 capability cards (AST pipeline, LLM pass, scoring, MCP, spec memory, multi-org) |
| Self-improving feedback loop | Circular 6-step diagram showing how every PR makes the next one smarter |
| Metrics | 6 KPI cards (false positive rate, noise reduction, PR cycle time, repeat violations, amendment adoption, escalation resolution) |
| MCP tools | Table of all 6 MCP tools with when-to-call and value description |
| Signals | 4 Spec Memory signals (S1 do_not_flag · S2 skip_ast_overlap · S3 canonical_id · S4 escalate) |
| Open-source | Public core vs. private cloud split explanation + quick-start commands |
| Success timeline | 6-month noise-reduction arc with bar chart |
| CTA | Install GitHub App + star repo links |

## Running locally

```bash
# Simple — just open in a browser
open index.html

# Or with Python for proper MIME types
python3 -m http.server 8080
# → http://localhost:8080
```

No build step required. Pure HTML + CSS, zero JavaScript dependencies.

## Deploying

Push this folder's contents to the root of the `GovuxAI/GovuxAI.github.io` repository.  
GitHub Pages serves `index.html` automatically.

```bash
# If this folder is already tracked in a repo:
git add .
git commit -m "update landing page"
git push origin main
```

Or, if setting up for the first time:

1. Create a new GitHub repository named **`GovuxAI.github.io`** under the `GovuxAI` organisation.
2. Push this folder's contents to the `main` branch.
3. In repo **Settings → Pages**, set Source to `main` / `/ (root)`.
4. The site goes live at `https://GovuxAI.github.io` within ~60 seconds.

## File structure

```
GovuxAI.github.io/
├── index.html      # Full single-page site
├── styles.css      # Design system (dark theme, CSS variables)
├── _config.yml     # Jekyll config (title / description / URL)
└── README.md       # This file
```

## Design tokens (CSS variables)

| Variable | Value | Usage |
|----------|-------|-------|
| `--bg` | `#0d0f14` | Page background |
| `--bg-2` | `#131720` | Section alternating background |
| `--bg-3` | `#1a1f2e` | Card / panel background |
| `--accent` | `#7c6bff` | Primary purple |
| `--accent-2` | `#a78bfa` | Light purple (code, links) |
| `--green` | `#4ade80` | Success / score high |
| `--red` | `#f87171` | Error / score low |
| `--yellow` | `#fbbf24` | Warning |
| `--text` | `#e2e8f0` | Primary text |
| `--text-2` | `#94a3b8` | Secondary text |
| `--text-3` | `#64748b` | Muted / captions |
