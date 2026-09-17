# Reviews

Adversarial scar tissue for `municipal-audits`.

This tree is **not** Findings. It is attack surface, named as such, so the Steward can close leaves without cosplay.

## Tree

```
reviews/
  README.md                          ← you are here
  adversarial/
    README.md                        ← how adversarial reviews work
    by-severity/
      kill-shots/                    ← free gimmes / case-killers
      medium/                        ← real damage, not fatal alone
      survives/                      ← what still stands after cheap shots
    by-target/
      repo-surface/                  ← README, naming, genre (“audit”)
      disclosures/                   ← legal / voice shields
      taxonomy/                      ← FIPS / COG / topics
      case-001-bartlett/             ← first case
      product/                       ← paid-audit sellability
      namespace/                     ← org / account optics
    by-date/
      2026-09-17/                    ← first pass (low-hanging fruit)
    open/                            ← unresolved leaves (symlinks via INDEX)
    closed/                          ← Steward-accepted remediations
  demands/
    sellable-bar.md                  ← what “done enough to sell” means
```

## Rules

1. **Name the genre.** Files say `adversarial` when they are adversarial.
2. **Low-hanging fruit stays labeled.** Cheap shots get `low-hanging-fruit` in path or title — no laundering into “peer review.”
3. **One leaf, one attack.** Close or reject per leaf; don’t rewrite history.
4. **Not Findings.** Promotion requires Steward Decision + typed evidence elsewhere.
5. **Date folders are append-only.** New passes get new dates.
6. **Scar and stitch.** Adversarial leaves without remediation are incomplete. See [`adversarial/SCAR-AND-STITCH.md`](adversarial/SCAR-AND-STITCH.md).
7. **Check your own work.** Every stitch needs a cold self-check. See [`adversarial/CHECK-YOUR-OWN-WORK.md`](adversarial/CHECK-YOUR-OWN-WORK.md).

## Start here

- Latest pass: [`adversarial/by-date/2026-09-17/`](adversarial/by-date/2026-09-17/)
- Kill shots only: [`adversarial/by-severity/kill-shots/`](adversarial/by-severity/kill-shots/)
- Sellable bar: [`demands/sellable-bar.md`](demands/sellable-bar.md)
