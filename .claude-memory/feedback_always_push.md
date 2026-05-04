---
name: Always push to remote
description: User wants every commit followed by git push immediately, no confirmation
type: feedback
originSessionId: ab24a770-ef29-4d8f-a3b0-b72b60164798
---
Always push to remote after committing changes.

**Why:** User's deployment flows depend on the remote being current — site (when public on Pages) goes live only after push, and the new device picks up changes via git pull. Currently the site is private and Pages is offline (see state_handoff), but the rule still applies for whatever host comes next.

**How to apply:** After every `git commit`, run `git push` immediately. Don't ask for confirmation. Applies to both `yoga-landing` and `yoga-bot` repos.
