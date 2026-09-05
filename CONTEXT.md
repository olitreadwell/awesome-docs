# testthedocs/awesome-docs context
> refreshed 2026-09-05 | upstream default: main @ de79bfe

## Identity & policies
- upstream: testthedocs/awesome-docs, default branch main, primary language Markdown (awesome-list), English-first (yes — README/CONTRIBUTING/issues all English).
- CLA/DCO: none (no CLA bot, no DCO requirement found).
- AI-assisted PR policy: unstated (no AI policy in repo or org files; no AI labels).
- signed commits required: no.
- PR template: `.github/PULL_REQUEST_TEMPLATE.md` (simple "Pull Request / Description" template, filled verbatim).
- external tracker: GitHub only.
- Maintainer: Sven (svx). CONTRIBUTING: every PR MUST be reviewed by at least two maintainers before merge; maintainers wait 30 days for interaction before closing.

## Conventions (verified from merged PRs)
- branch naming: `add-<name>` / `<username>/add-<name>` for additions (e.g. add-eziwiki, agent/add-canopy, add-notula); fall back to `fix/<desc>` for fixes.
- commit style: plain imperative, no Conventional-Commits prefix ("Add X to ...", "Fix ...").
- list rules (CONTRIBUTING): items sorted alphabetically per category; one link per item; link = project name; description on same line ending with punctuation; >=3 items make a category.
- CI: `.github/workflows/linkcheck-on-pr.yml` (lychee, fail:true) and cron-linkcheck are BOTH `disabled_manually` on upstream — maintainers turned link checking off (noisy on false-positive 403s). No other PR-gating CI. So a fork PR has no substantive CI to go green.
- alex (`.alexrc`) used for inclusive language; allow-list handyman-handywoman + postman-postwoman.

## Maintainer picture
- Single listed maintainer Sven (svx); issues/PRs addressed irregularly; recent merges of external "add X" PRs are common and quick.

## Issue-area health
- Open issues are almost all "Add <tool>"/suggestion entries (e.g. #122 Add Agent QA, #113 Add Text to Confluence) or open-ended discussions (#28 alphabetize, #29 add descriptions). No maintainer-engaged actionable bug/approved issue survives as a small pick.
- Dead-link handling precedent: issue #52 "docz redirects to a site about OF" (2025-10-11) — link was subsequently removed; maintainers do act on dead links.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-09-05` self-found gap — dead link AsciiDoc Alive (`https://asciidocalive.docswriter.com/`, README line 59): TLS certificate EXPIRED (lychee: "SSL certificate expired"; curl fails exit 60; browser cannot load). Verified live against current upstream de79bfe. Deduped: no upstream issue/PR touches this. Fix: point to verified-200 Wayback snapshot `https://web.archive.org/web/20260311230934/https://asciidocalive.docswriter.com/` (title AsciiDocAlive, 200). Excluded as false positives: 9× HTTP 403 on major live sites (medium, quillbot, salesforce, splunk, linode, acm, stylepedia, capitalizemytitle, divtable) and github.com 429s — bot-block/rate-limit, left untouched. — status: proposed

## Mined gaps (discovered, not yet attempted)
- `2026-09-05` docs — entire README (287 unique links) curl-scanned; only genuine dead link is the AsciiDoc Alive cert-expired URL above; no 404/410/NXDOMAIN found. — status: attempted (see ledger)
