---
id: KS-004
tier: kill-shot
tags: [low-hanging-fruit, metadata, credibility]
targets: [case-001-bartlett, repo-surface]
date: 2026-09-17
status: open
---

# KS-004 — `privacy_class: public-rendition-pending` while tree is public

Self-inflicted credibility cut.

**Remediation:** Set `privacy_class: public` (or `public-methodology-sample`) and note what remains withheld, if anything.

## Self-check
1. Read `privacy_class` (or equivalent) on CASE.md / Aletheia header.
2. Confirm the GitHub tree visibility.
3. **Pass:** metadata says `public` (or accurate hybrid) matching reality.
4. **Fail:** `public-rendition-pending` while the repo is already public.
