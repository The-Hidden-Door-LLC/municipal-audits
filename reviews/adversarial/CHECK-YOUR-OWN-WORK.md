# Check your own work

**Standing method.** After a stitch, the subject must be able to re-verify without Hidden Door present.

This is not “trust us.” It is a repeatable checklist so a city clerk, finance director, Steward, or buyer can fail closed on their own.

## Principle

If you cannot re-run the check and get a yes/no from **public locators + dated retrieval**, you did not fix it — you performed.

## Universal self-check (every open-books case)

Run cold. No Inside Knowledge. Browser or curl only.

### A. Genre honesty
1. Open the case `CASE.md` and repo README.
2. Note the claimed genre (`audit` vs `publication surface review`).
3. **Pass:** claim matches what exists (captures + rendition if “audit”).
4. **Fail:** word “audit” with only a one-day web skim.

### B. Macro books present
1. From the city domain, open Finance / Budget / ACFR (or equivalent).
2. Download current adopted budget PDF and latest ACFR/CAFR.
3. Record URL, retrieval date, file size; hash if you keep evidence (`shasum -a 256`).
4. **Pass:** files open, dates match the fiscal year claimed in the case.
5. **Fail:** broken links, “coming soon,” or wrong year sold as current.

### C. Payment layer (the actual question)
1. Search the city site for: check register, AP payments, vendor payments, open checkbook, warrants, disbursements.
2. Search bid/award pages for **awardee names + amounts**, not only solicitation titles.
3. **Pass (published):** a public, dated payment-level artifact a stranger can open without logging a petition.
4. **Pass (honest gap):** no such artifact — case labels `EvidenceGap`, not “hidden crime.”
5. **Fail:** case implies payees are public when only NextRequest/FOIA paths exist.

### D. Petition ≠ publication (method check)
1. Open the public-records portal (if any). Note residency, fees, login.
2. **Pass:** case treats portal as process friction / optional channel, not as “already open.”
3. **Fail:** scorecard credits portal presence as payment-layer transparency.

### E. Independence / appearance (Steward cases)
1. Read case disclosures for conflict-appearance language when Steward has parallel matters touching the same city.
2. **Pass:** facts disclosed or Steward Decision “withheld, reason X” on file.
3. **Fail:** silence while personal and product timelines collide.

### F. Rendition test (can a stranger use it?)
1. Open `renditions/` (or the linked scorecard).
2. In ≤2 minutes, answer: what is published / petition-only / not found?
3. **Pass:** one page, three columns (or equivalent), dated.
4. **Fail:** only a long Aletheia file, no forwardable scorecard.

### G. Taxonomy anchors
1. Primary COG/FIPS codes match the place and the question.
2. Secondary function codes either cite budget lines or are absent.
3. **Fail:** decorative Census codes with no line-item pin.

## Per-leaf self-check

Every `KS-*` / `MD-*` leaf should add a short **Self-check** block:

```markdown
## Self-check
1. …
2. …
**Pass:** …
**Fail:** …
```

If the leaf has remediation but no self-check, it is still incomplete under [`SCAR-AND-STITCH.md`](SCAR-AND-STITCH.md).

## Cadence

- After each stitch: run the relevant letters (A–G) same day.
- Before invoice / public “audit” claim: full A–G, cold, by someone who did not write the case.
- Quarterly (product): re-run C–D on active cases — cities change portals.

## What self-check is not

- Not a TPRA legal opinion.
- Not permission to allege crime from a gap.
- Not a substitute for counsel when the Steward wants filings.
