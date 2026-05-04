---
name: Current state handoff (2026-05-04)
description: Snapshot of where work stopped — repos, hosting state, next steps. Verify before acting.
type: project
originSessionId: ab24a770-ef29-4d8f-a3b0-b72b60164798
---
State on **2026-05-04**, when user moved to another device.

## Repos (both private, on GitHub account `ahimsa2403`)
- **`ahimsa2403/yoga-landing`** — landing site (`index2.html`), working dir `/Users/chelios/Yoga site`
- **`ahimsa2403/yoga-bot`** — Python Telegram bot, working dir `~/projects/yoga-bot/` (kept separate, NOT inside landing repo)
- **`chev-chelios-tech/stasiya_yoga`** — old, archived, do not touch

## Hosting
- **Site is currently DOWN** — was on GitHub Pages, but Pages doesn't work for private repos on free GitHub plan. URL `https://ahimsa2403.github.io/yoga-landing/index2.html` returns 404.
- **Bot is not yet hosted** — needs free 24/7 host.
- User's intent: host site + bot in **one place**, both free, both private. Cloudflare Pages + Workers was discussed as best fit.

## Next steps (planned, not done)
1. Migrate site from GitHub Pages to **Cloudflare Pages** (works with private repos free)
2. Set up bot on **Cloudflare Workers** (webhook mode) or **Fly.io** (if polling) — same account so site+bot are in one dashboard

## Active gh account
`ahimsa2403`. Run `gh auth switch --user ahimsa2403` if not active. Auth scopes include `workflow`.

**Why:** Repos went private at user request; Cloudflare migration deferred to next device.
**How to apply:** On resume, first verify gh active account, then either continue Cloudflare migration or whatever user asks. Don't push to old `chev-chelios-tech/stasiya_yoga` repo — it's archived.
