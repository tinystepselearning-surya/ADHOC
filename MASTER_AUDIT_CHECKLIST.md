# Master Website Audit Checklist

Status: Sri Raama public website review in progress (started 2026-11-27 IST).
Scope: https://sriraama.in/ — factual observations from publicly accessible sources only. Repository is public by user choice; confidential material and private commercial strategy are excluded.

## Technical baseline — Phase 00

[SR-B00 — Preliminary technical baseline](baseline/SR-B00_TECHNICAL_BASELINE.md). In progress; bounded raw source crawl completed: 31 self-canonical pages, 32 distinct final HTML URLs, 35 successful candidate requests. Sitemap and robots policy verified. Rich results, rendered DOM, performance, Google indexing and real bot access remain pending. Technical findings use SR-B00-Fxx IDs; SR-001 remains recorded.

## Audit workstreams

| ID | Workstream | Status |
| --- | --- | --- |
| A01 | Content accuracy and editorial quality | In progress — 1 finding |
| A02 | Website completeness and missing pages | Pending |
| A03 | UI design, aesthetics and branding | Pending |
| A04 | UX and navigation | Pending |
| A05 | Mobile responsiveness | Pending |
| A06 | Technical SEO | In progress — source crawl completed; SR-B00-F02/F03 |
| A07 | On-page SEO | In progress — source baseline and SR-B00-F01 |
| A08 | Google rankings and organic visibility | Pending |
| A09 | Keyword strategy and content gaps | Pending |
| A10 | Local SEO and Google Maps | Pending |
| A11 | Competitor benchmarking | Pending |
| A12 | AEO and GEO readiness | Pending |
| A13 | Website speed and performance | Pending |
| A14 | Accessibility | In progress — source findings F01–F03; DOM testing pending |
| A15 | Admissions and lead generation | Pending |
| A16 | Analytics and conversion tracking | Pending |
| A17 | Technology, security and privacy | Pending |
| A18 | Maintenance, reporting and accountability | Pending |

## Findings register

| ID | Workstream | Finding | Severity | Evidence status | Review status | Detail |
| --- | --- | --- | --- | --- | --- | --- |
| SR-001 | A01 | NEET coaching listed on MPC–JEE programme page | High | Verified — retrieved text | Open | [Detail](findings/SR-001.md) |
| SR-B00-F01 | A07 / A14 | All 31 self-canonical pages lack native H1 headings in source | High (proposed) | Verified — source metrics | Open | [Detail](findings/SR-B00-F01.md) |
| SR-B00-F02 | A06 / A14 | Repeated HTML element IDs on all 31 canonical pages; 185 excess occurrences | Medium (proposed) | Verified — source counts; DOM scope pending | Open | [Detail](findings/SR-B00-F02.md) |
| SR-B00-F03 | A14 / A06 | Native main, header and footer elements absent on all 31 canonical pages | Medium (proposed) | Verified — native tag counts; ARIA and accessibility tree pending | Open | [Detail](findings/SR-B00-F03.md) |

## Finding record template

- Reference ID and workstream
- Affected URL(s), page section, observation date
- Expected behaviour and observed behaviour
- Evidence and reproducible verification steps
- Severity and rationale
- Potential business impact (distinguish measured from hypothetical)
- Specific review questions
- Supporting records requested
- Evidence status: verified / suspected / internal verification required
- Review status: open / answered / disputed / resolved
- Limitations, response and retest evidence

## Working rules

1. Investigate one finding at a time. Do not duplicate findings.
2. Record evidence before declaring a defect; distinguish retrieved text from actual screenshots.
3. Do not attribute fault, duration, ranking losses or commercial impact without evidence.
4. Record pending checks separately; unavailable data is not proof of failure.
5. Use read-only public checks. Do not submit live enquiries, conduct intrusive tests or change the audited website.
6. Do not store credentials, personal data, student records or confidential material in a public repository.
7. Preserve existing records and update the master register with each finding.
8. Finalise the management-review checklist only after reconciling findings, audit coverage and limitations.
9. Keep private commercial proposals and growth strategy outside the existing-team review materials.
