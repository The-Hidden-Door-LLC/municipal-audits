---
schema_version: aletheia-protocol/0.5
document_id: bartlett-open-books-evidence-record
version: 1
status: active
document_class: informative
project_id: bartlett-open-books
privacy_class: project-private
steward: Kathy Hoff
created_at: 2026-09-17
created_by: Grok Bot (AI contributor) under instruction of the Steward
protocol_source: https://github.com/KarstenEvans/aletheia-protocol (specification 0.5.0-rc.2, as adopted by the Steward in hoff-v-spiller-evidence-record and complaint-2607180152-evidence-record)
mandatory_conflict_retrieval: true
---

# Evidence Record — Bartlett Open Books / Public Records Access

IA-BARTLETT-001.

This record concerns whether the City of Bartlett, Tennessee publishes the transaction layer of public finance, or walls records that Tennessee already treats as public behind petition, residency gate, and labor fee.

This record does not accuse a crime. It types what is published, what is absent, what the City claims, and where those collide. Promotion from Hypothesis to Finding requires evidence registered here.

Knowledge belongs to the project, not the Assistant.

---

## 0. Adoption and conformance declaration

```yaml
adoption: adopted
conformance: core
profile: null
scope: this evidence record only
omitted_full_requirements:
  - per-node revision_id, previous_revision_id and body_sha256 (not yet implemented;
    file-level digests to be added when local captures are saved under evidence/)
  - valid_from / valid_until on individual nodes (time is stated in node text where it matters)
agentic_systems_profile: not adopted — no external filings, NextRequest submissions,
  or contact with City staff are authorized by this record unless the Steward accepts
  a Decision node that says so
```

## 0.1 Roles

| Role | Holder |
|---|---|
| Steward | Kathy Hoff — accepts or rejects every change to this record |
| Contributor | Grok Bot (AI), session 2026-09-17 |
| Reviewer | not engaged |
| Custodians (subject-side) | City of Bartlett Finance Department · City Clerk · Fleet Services · Purchasing · Board of Mayor and Aldermen |
| Comparative custodians | City of Memphis (Open Checkbook / transparency surfaces) · Shelby County (contracts data portal) |

## 0.2 Non-negotiable distinctions

Inherited from the Steward's prior Aletheia records and binding here.

- Evidence is not interpretation. A URL that returns a budget PDF is Evidence of publication of that PDF, not proof the City is transparent.
- Statements by City staff, elected officials, or portal copy are **Claims by the City** (or by the named speaker). They do not become fact by being quoted.
- Absence of a public check register, after documented search, is an **EvidenceGap** and may support a **Hypothesis**. It is not, by itself, proof of concealment-with-intent.
- A SHA-256 match shows only that a captured file is unchanged. It does not show the file's contents are true.
- **Quote exactly.** Paraphrase of City policy language is forbidden in nodes that carry legal or policy weight.
- Memphis / Shelby comparisons are **Observations** of other jurisdictions' publication surfaces, not Findings that Bartlett is "tainted" unless separately supported.
- This record is not legal advice. Legal conclusions are Questions for counsel (§8).

---

## 1. Project specification

**Intention.** Preserve and organise the evidence concerning Bartlett's publication of municipal financial and purchasing records — especially payment-level vendor data and fleet-related spend — so that every statement about "open books" or "locked records" can be tested against a locator.

**Success criteria.** (1) Every material statement traces to a node here. (2) Every Evidence node traces to a locator a third party can open. (3) Every known conflict carries all its sides. (4) Every missing ledger class is an EvidenceGap, not a silence. (5) No NextRequest is treated as the cure for non-publication; process friction may be Evidence of a wall, not a solution path baked into the finding.

**Scope.** City of Bartlett, Tennessee. Public web corpus and municipal code as retrieved 2026-09-17. Focus exemplar: fleet / vehicle maintenance spend and vendor identity. Comparative reference: Memphis Open Checkbook surfaces; Shelby County contracts portal. Temporal window: FY2024 through FY2026 YTD materials found published as of 2026-09-17.

**Exclusions.** Individual employee private personnel data. Active law-enforcement investigative files. The Steward's separate criminal, civil, or family matters (complaint-2607180152; hoff-v-spiller; others) except where a publication practice collides with those cases by Decision of the Steward. No contact with City staff unless authorized.

**Constraints.** con-001 through con-004 (§6).

---

## 2. Evidence register

Retrieval date for web locators in this section: **2026-09-17** (America/Chicago), unless a node says otherwise. Integrity digests: pending local capture.

```yaml
- evidence_id: ev-city-site
  title: City of Bartlett official website (CivicPlus)
  source_class: primary
  creator_or_speaker: City of Bartlett
  knowledge_basis: direct retrieval
  source_created_at: unknown
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartlett.org/"}
  alternate_uri: "https://www.cityofbartlett.org/"
  integrity: {algorithm: none, digest: null}
  claim_scope: existence and structure of the City's public web publication surface
  limitations: [CivicPlus CMS; content can change without notice; homepage is not a financial ledger]

- evidence_id: ev-finance-dept
  title: Finance Department page — budgets, ACFRs, monthly financial reports
  source_class: primary
  creator_or_speaker: City of Bartlett Finance Department
  knowledge_basis: direct retrieval
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartlett.org/19/Finance-Department"}
  integrity: {algorithm: none, digest: null}
  claim_scope: the City publishes multi-year adopted budget PDFs and ACFR/CAFR PDFs from this hub
  limitations: [line items are departmental aggregates; payees are not identified on these PDFs]

- evidence_id: ev-budget-fy2026
  title: Fiscal 2026 Adopted Budget (PDF referenced via Finance DocumentCenter)
  source_class: primary
  creator_or_speaker: City of Bartlett
  knowledge_basis: secondary report of DocumentCenter identifiers pending local PDF capture
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartlett.org/19/Finance-Department", note: "FY2026–27 materials linked from Finance hub; local PDF capture pending as ev-budget-fy2026-file"}
  integrity: {algorithm: none, digest: null}
  claim_scope: adopted appropriations including Vehicle Maintenance aggregates
  limitations: [Contributor summary cited General Fund Vehicle Maintenance $536,300; Public Safety $351,500; Public Works $134,300; Solid Waste Fund $625,000 — VERIFY against PDF before promoting to Measurement nodes]
  steward_review: required

- evidence_id: ev-acfr-fy2025
  title: ACFR / annual comprehensive financial report FY2025 (DocumentCenter)
  source_class: primary
  creator_or_speaker: City of Bartlett
  knowledge_basis: URI identified 2026-09-17; local capture pending
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartlett.org/DocumentCenter/View/6713"}
  integrity: {algorithm: none, digest: null}
  claim_scope: audited financial statements as published
  limitations: [ACFR is not an AP check register]

- evidence_id: ev-purchasing
  title: Purchasing page
  source_class: primary
  creator_or_speaker: City of Bartlett
  retrieved_at: 2026-09-17
  locator: {uri: "https://www.cityofbartlett.org/1205/Purchasing"}
  integrity: {algorithm: none, digest: null}
  claim_scope: points to sealed bids / RFPs workflow
  limitations: [does not itself list payees]

- evidence_id: ev-bids
  title: CivicEngage bid postings index
  source_class: primary
  creator_or_speaker: City of Bartlett
  retrieved_at: 2026-09-17
  locator: {uri: "https://www.cityofbartlett.org/bids.aspx"}
  integrity: {algorithm: none, digest: null}
  claim_scope: historical bid solicitations are published; closed/awarded/cancelled toggle exists
  limitations: [award vendor names often absent from listing page; solicitations ≠ payment ledger]

- evidence_id: ev-bids-fleet-cat
  title: Fleet-category bid solicitations (CatID=30)
  source_class: primary
  creator_or_speaker: City of Bartlett
  retrieved_at: 2026-09-17
  locator: {uri: "https://www.cityofbartlett.org/Bids.aspx?CatID=30&Status=&showAllBids=on&txtSort=BidNumberAsc"}
  integrity: {algorithm: none, digest: null}
  claim_scope: fleet-tagged IFBs exist (oil, lubricants, transmission, diesel rebuild, parts, software, lifts, refuse trucks, etc.)
  limitations: [counts and titles require live re-fetch before Measurement; awardees not established by this index alone]

- evidence_id: ev-fleet-services
  title: Fleet Services division page
  source_class: primary
  creator_or_speaker: City of Bartlett Fleet Services
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartlett.org/473/Fleet-Services"}
  integrity: {algorithm: none, digest: null}
  claim_scope: City describes an in-house garage maintaining city motorized assets; published contacts and counts on page as of retrieval
  limitations: [page claims are Claims by the City; outside vendor spend is not itemized here]

- evidence_id: ev-city-clerk
  title: City Clerk / public records page
  source_class: primary
  creator_or_speaker: City of Bartlett City Clerk
  retrieved_at: 2026-09-17
  locator: {uri: "https://www.cityofbartlett.org/290/City-Clerk"}
  integrity: {algorithm: none, digest: null}
  claim_scope: states fees and links to NextRequest; identifies records coordinator contacts as published
  limitations: [fee schedule must be quoted from page capture before use in any public rendition]

- evidence_id: ev-nextrequest
  title: Bartlett NextRequest public records portal
  source_class: primary
  creator_or_speaker: City of Bartlett (NextRequest platform)
  retrieved_at: 2026-09-17
  locator: {uri: "https://cityofbartletttn.nextrequest.com/"}
  integrity: {algorithm: none, digest: null}
  claim_scope: existence of a petition portal for TPRA requests; cites Resolution 24-17 on portal copy
  limitations: [a portal for requesting records is not proactive publication of those records; Resolution 24-17 PDF not located on city site in the 2026-09-17 pass]

- evidence_id: ev-civicclerk
  title: CivicClerk agendas and minutes portal
  source_class: primary
  creator_or_speaker: City of Bartlett
  retrieved_at: 2026-09-17
  locator: {uri: "https://bartletttn.portal.civicclerk.com/"}
  integrity: {algorithm: none, digest: null}
  claim_scope: board packets and meeting files are published here
  limitations: [award letters / POs may appear piecemeal if at all; not a substitute for AP register]

- evidence_id: ev-title5-code
  title: Municipal code Title 5 — Municipal Finance and Taxation (DocumentCenter)
  source_class: primary
  creator_or_speaker: City of Bartlett
  retrieved_at: 2026-09-17
  locator: {uri: "https://www.cityofbartlett.org/DocumentCenter/View/10513/Title-5---Municipal-Finance-and-Taxation"}
  integrity: {algorithm: none, digest: null}
  claim_scope: code language regarding Registry of Suppliers and purchase-transaction records for public inspection (exact text requires quote from PDF)
  limitations: ["for public inspection" ≠ machine-readable public export; PDF quote pending]

- evidence_id: ev-memphis-transparency-hub
  title: City of Memphis budgets / transparency hub (comparative)
  source_class: secondary
  creator_or_speaker: City of Memphis
  retrieved_at: 2026-09-17
  locator: {uri: "https://memphisgov.com/budgets-transparency"}
  integrity: {algorithm: none, digest: null}
  claim_scope: Memphis markets transaction-level openness / Open Checkbook style surfaces (page fetch returned errors in one pass; existence reported via search indexes)
  limitations: [live verification of Open Checkbook filters/CSV export still required; do not overclaim]

- evidence_id: ev-shelby-contracts
  title: Shelby County Contracts Data Portal (comparative)
  source_class: primary
  creator_or_speaker: Shelby County
  retrieved_at: 2026-09-17
  locator: {uri: "https://contracts.shelbycountytn.gov/"}
  integrity: {algorithm: none, digest: null}
  claim_scope: searchable master contracts list with vendor, amount, dates
  limitations: [County ≠ City of Bartlett; comparison is publication-practice only]

- evidence_id: ev-daily-memphian-chamber
  title: Daily Memphian coverage — Bartlett Area Chamber funding controversy
  source_class: secondary
  creator_or_speaker: Daily Memphian
  retrieved_at: 2026-09-17
  locator: {uri: "https://dailymemphian.com/article/52426/bartlett-chamber-of-commerce-under-fire"}
  related_uri: "https://dailymemphian.com/article/52602/clay-bailey-bartlett-alderman-david-reaves-bartlett-chamber"
  integrity: {algorithm: none, digest: null}
  claim_scope: recent local reporting on city funding oversight of Chamber — spending politics, not FOIA-war
  limitations: [journalism is secondary; not evidence of fleet-vendor identity]
```

---

## 3. Claims register

```yaml
- claim_id: cl-city-macro-open
  speaker: City of Bartlett (by publication practice)
  statement: Adopted budgets, ACFRs, and related finance PDFs are posted for public download.
  truth_status: provisional
  support: [ev-finance-dept, ev-budget-fy2026, ev-acfr-fy2025]
  limitations: [publication of aggregates is not publication of payees]

- claim_id: cl-city-records-via-portal
  speaker: City of Bartlett (City Clerk page / NextRequest copy)
  statement: Public records may be requested through the NextRequest portal under TPRA / Resolution 24-17.
  truth_status: provisional
  support: [ev-city-clerk, ev-nextrequest]
  limitations: [availability-by-petition is not the same proposition as default publication]

- claim_id: cl-fleet-inhouse
  speaker: City of Bartlett Fleet Services page
  statement: Fleet Services maintains and repairs city motorized assets at a City garage (published address/contacts/counts on page).
  truth_status: provisional
  support: [ev-fleet-services]
  limitations: [does not negate outside vendor spend on parts, rebuilds, software, or overflow work]
```

---

## 4. Hypotheses (not findings)

```yaml
- hypothesis_id: hyp-001
  title: Macro-open, payment-opaque
  statement: Bartlett publishes macro budgets and audited statements while withholding payment-level vendor data that peer metro governments publish.
  truth_status: provisional
  support: [ev-finance-dept, ev-acfr-fy2025, gap-ap-register, ev-memphis-transparency-hub, ev-shelby-contracts]
  conflict_set: [cfl-001]
  steward_review: required

- hypothesis_id: hyp-002
  title: Petition as wall
  statement: NextRequest plus residency and labor-fee rules function as practical friction around records that are already public under Tennessee law.
  truth_status: provisional
  support: [ev-nextrequest, ev-city-clerk, gap-ap-register]
  conflict_set: [cfl-001]
  steward_review: required

- hypothesis_id: hyp-003
  title: Fleet payees unpublished
  statement: Fleet / vehicle maintenance is budgeted in aggregate; current outside vendor identities and dollar payouts are not available on the open web corpus surveyed 2026-09-17.
  truth_status: provisional
  support: [ev-fleet-services, ev-bids-fleet-cat, gap-fleet-payees, ev-budget-fy2026]
  conflict_set: []
  steward_review: required

- hypothesis_id: hyp-004
  title: Code promises inspection, web withholds export
  statement: Title 5 contemplates supplier registry / purchase-transaction records for public inspection, while no machine-readable public export of those records was found.
  truth_status: provisional
  support: [ev-title5-code, gap-supplier-registry-export, gap-ap-register]
  conflict_set: []
  steward_review: required
```

**Rejected as opening finding (must remain visible):** that Bartlett is "corrupt," "criminal," or "tainted by Bluff City" in a moral or prosecutorial sense. Those are not Findings of this record. Metro comparison is publication-practice only (obs-001).

---

## 5. Observations

```yaml
- observation_id: obs-001
  statement: As of 2026-09-17 search/retrieval, Memphis markets transaction-level transparency surfaces and Shelby County publishes a searchable contracts portal; Bartlett's surveyed public surface is budget/ACFR/bids/agendas without a public AP checkbook.
  source_refs: [ev-memphis-transparency-hub, ev-shelby-contracts, gap-ap-register, gap-contracts-db]
  truth_status: provisional
  limitations: [Memphis hub fetch error in one pass; re-verify before public rendition]

- observation_id: obs-002
  statement: No dedicated citywide "Open Data" / "Transparency checkbook" / Laserfiche public AP portal was found on the Bartlett web corpus surveyed 2026-09-17.
  source_refs: [ev-city-site, ev-finance-dept, gap-ap-register]
  truth_status: provisional
```

---

## 6. Constraints

```yaml
- constraint_id: con-001
  statement: No NextRequest filing, email to City staff, or other external process act without an accepted Decision node by the Steward.

- constraint_id: con-002
  statement: Do not treat FOIA/TPRA procedure as the remedy inside Findings; procedure may be Evidence of friction (hyp-002).

- constraint_id: con-003
  statement: Do not merge this project with complaint-2607180152, hoff-v-spiller, or other Steward matters unless the Steward accepts a Decision that says so.

- constraint_id: con-004
  statement: Privacy class remains project-private until the Steward accepts a public rendition Decision.
```

---

## 7. Conflicts

```yaml
- conflict_id: cfl-001
  title: Availability-by-petition vs default publication
  sides:
    - side: City process claim
      claim_ref: cl-city-records-via-portal
      paraphrase_forbidden: true
      gist: Records can be obtained through NextRequest / clerk process under TPRA.
    - side: Open-books hypothesis
      hypothesis_ref: hyp-002
      gist: If a record is public, requiring petition, residency proof, and labor fees to see payees is a wall, not openness.
  status: unresolved
  retrieval_rule: both sides MUST be retrieved whenever either is used
```

---

## 8. Evidence gaps

```yaml
- gap_id: gap-ap-register
  expected_evidence: Accounts Payable check registers / vendor payment reports / electronic disbursement listings (preferably CSV/Excel), especially Fleet Services / Public Works Shop, FY2024–FY2026 YTD
  why_expected: Budget PDFs show Vehicle Maintenance appropriations; payment-level data is the ordinary next cell in an open ledger
  likely_custodian: Finance Department / City Clerk
  attempts: [public web survey 2026-09-17 — not found on city site]
  consequence: hyp-001 and hyp-003 cannot be closed; payee identity remains unknown
  resolution_routes: [City Hall inspection of purchase-transaction file per Title 5, Steward-authorized only] [Board packet dig via CivicClerk] [NOT defaulted to NextRequest as "the answer"]
  review_due: 2026-10-01

- gap_id: gap-fleet-payees
  expected_evidence: Award letters, POs, and current contracts for oil/lubricants, vehicle parts, transmission repair, diesel rebuild, vehicle maintenance software
  why_expected: Fleet-category IFBs exist (ev-bids-fleet-cat); awards and payments should exist somewhere
  likely_custodian: Purchasing / Fleet / City Clerk
  attempts: [bid index review 2026-09-17 — solicitations found, awardees not established]
  consequence: outside vendor names remain EvidenceGap
  resolution_routes: [CivicClerk packet search] [DocumentCenter award PDFs if any] [inspection]
  review_due: 2026-10-01

- gap_id: gap-contracts-db
  expected_evidence: Searchable public contracts / PO database comparable to Shelby County's portal
  why_expected: Peer metro government publishes one
  likely_custodian: City of Bartlett / IT / Purchasing
  attempts: [web survey 2026-09-17 — not found]
  consequence: obs-001 comparison stands on absence
  resolution_routes: [confirm continued absence on re-fetch] [Steward Decision on public scorecard]
  review_due: 2026-10-01

- gap_id: gap-supplier-registry-export
  expected_evidence: Machine-readable export of Registry of Suppliers / purchase-transaction file referenced by Title 5
  why_expected: Code language indicates such records exist for inspection
  likely_custodian: Finance / City Clerk
  attempts: [no public export found 2026-09-17]
  consequence: hyp-004 remains open
  resolution_routes: [quote exact Title 5 text into Evidence] [inspection — Steward-gated]
  review_due: 2026-10-01

- gap_id: gap-resolution-24-17-pdf
  expected_evidence: Resolution 24-17 Public Records Policy PDF
  why_expected: Cited on NextRequest portal copy
  likely_custodian: City Clerk
  attempts: [not found on city site in 2026-09-17 pass]
  consequence: fee/residency rules cannot be quoted from the controlling resolution yet
  resolution_routes: [DocumentCenter / CivicClerk search] [capture portal text as Claim by City with screenshot]
  review_due: 2026-09-24
```

---

## 9. Timeline

Append-only. Do not rewrite past events; supersede with new nodes.

```yaml
- event_id: t-2026-09-17-a
  at: 2026-09-17
  type: Action
  actor: Grok Bot (Contributor) under Steward conversation
  statement: Public web survey of Bartlett finance, fleet, bids, clerk, and NextRequest surfaces completed; comparative Memphis/Shelby locators noted.
  source_refs: [ev-city-site, ev-finance-dept, ev-fleet-services, ev-bids, ev-nextrequest]

- event_id: t-2026-09-17-b
  at: 2026-09-17
  type: Decision
  actor: Steward Kathy Hoff
  statement: Steward directed Contributor to write this Aletheia evidence record and to let the record speak in its own voice.
  source_refs: []

- event_id: t-2026-09-17-c
  at: 2026-09-17
  type: Action
  actor: Grok Bot (Contributor)
  statement: Opened bartlett-open-books_Evidence-Record.aletheia.md version 1 under Cases/bartlett-open-books/.
  source_refs: []
```

---

## 10. Questions for counsel / Steward

```yaml
- question_id: q-001
  audience: Steward
  question: Confirm project_id caption `bartlett-open-books` and privacy_class `project-private` until a public rendition is accepted.

- question_id: q-002
  audience: Steward
  question: Authorize, or refuse, local PDF captures (budget, ACFR, Title 5) into evidence/ with SHA-256 — still no NextRequest.

- question_id: q-003
  audience: Steward
  question: Authorize, or refuse, CivicClerk packet dig for fleet award names (read-only public web).

- question_id: q-004
  audience: counsel (if engaged)
  question: Under TPRA and Bartlett Title 5, what is the legal distinction between "public inspection at City Hall" and "proactive machine-readable publication," and what remedies exist for systematic non-publication of AP registers?
```

---

## 11. Pending proposals (no silent rewrite)

```yaml
- proposal_id: prop-001
  target_node: ev-budget-fy2026
  change_type: revise
  reason: Replace DocumentCenter-hub reference with captured PDF + SHA-256 and promote Vehicle Maintenance figures to Measurement nodes only after byte-level verify
  decision: pending
  proposed_by: Grok Bot
  proposed_at: 2026-09-17

- proposal_id: prop-002
  target_node: null
  change_type: revise
  reason: Add evidence/ folder captures for Title 5 PDF and ACFR FY2025
  decision: pending
  proposed_by: Grok Bot
  proposed_at: 2026-09-17
```

---

## 12. Provenance trace (this version)

```yaml
task: Open IA-BARTLETT-001 Aletheia evidence record per Steward instruction 2026-09-17
corpus_supplied: Steward conversation establishing Bartlett focus; Contributor web survey 2026-09-17; Steward's prior Aletheia record shapes (complaint-2607180152; hoff-v-spiller)
retrieval_mode: dual
included_anchors: [ev-finance-dept, ev-fleet-services, ev-bids, ev-nextrequest, ev-title5-code, gap-ap-register]
mandatory_conflicts_retrieved: [cfl-001]
material_exclusions: [no NextRequest filing; no merge with Steward criminal/civil case files]
uncertainty: [Memphis transparency hub live behavior; exact Vehicle Maintenance dollar figures pending PDF verify; Resolution 24-17 PDF missing]
unavailable_sources: [AP register, fleet payee awards, contracts DB export]
```

---

## 13. Human Steward-review points

1. Accept or reject version 1 as the project source of truth.
2. Decide prop-001 / prop-002 (local PDF captures).
3. Decide q-003 (CivicClerk award dig) without treating NextRequest as the default move.
4. Keep hyp-001–004 labeled Hypothesis until EvidenceGaps close or are accepted as standing absences for a public scorecard rendition.

---

*Working motto (Aletheia): Remember well. Reason clearly. Prosper together.*

*This record speaks for the project. The Assistant does not own it.*
