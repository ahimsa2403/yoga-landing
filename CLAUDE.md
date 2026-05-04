# Yoga site project

Single-file landing for yoga teacher Stasyia. Live entry point: `index2.html`.

## Repos
- **This repo:** `ahimsa2403/yoga-landing` (private)
- **Bot:** `ahimsa2403/yoga-bot` (private, separate repo, lives outside this dir)
- Old archived repo: `chev-chelios-tech/stasiya_yoga` — do not push to it.

## Active GitHub account
`ahimsa2403`. If `gh auth status` shows another active account, run:
```
gh auth switch --user ahimsa2403
```

## Hosting status (as of 2026-05-04)
Site is **not currently live** — was on GitHub Pages, but Pages doesn't support private repos on free plan. Migration to **Cloudflare Pages** planned (works with private repos free, same dashboard for the bot via Workers).

## Memory directory
Claude Code's auto-memory for this project is committed to `.claude-memory/` and symlinked into `~/.claude/projects/-Users-chelios-Yoga-site/memory`. On a fresh machine after cloning:
```bash
ln -s "$(pwd)/.claude-memory" ~/.claude/projects/-Users-chelios-Yoga-site/memory
```
(Path of `~/.claude/projects/-Users-chelios-Yoga-site/` will appear after first Claude Code run; create it if missing.)

## Push rule
Every commit is followed by `git push` immediately. No confirmation needed.
