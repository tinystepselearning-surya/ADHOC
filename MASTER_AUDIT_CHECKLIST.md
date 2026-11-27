# Master Website Audit Checklist

Status: Sri Raama public website review in progress (started 2026-11-27 IST).
Scope: https://sriraama.in/ — factual observations from publicly accessible sources only. Repository is public by user choice; confidential material and private commercial strategy are excluded.

## Technical baseline — Phase 00

[SR-B00 — Preliminary technical baseline](baseline/SR-B00_TECHNICAL_BASELINE.md). In progress; bounded raw source crawl completed: 31 self-canonical pages, 32 distinct final HTML URLs, 35 successful candidate requests. Sitemap and robots policy verified. Rich results, rendered DOM, performance, Google indexing and real bot access remain pending. Technical findings use SR-B00-Fxx IDs; SR-001 remains recorded.

## Independent validation

[SR-B01 — Independent validation progress](baseline/SR-B01_INDEPENDENT_VALIDATION.md). Performance collection blocked externally; public search discovery sample and content checks started. No measured ranking or speed claims.

## Audit workstreams

| ID | Workstream | Status |
| --- | --- | --- |
| A01 | Content accuracy and editorial quality | In progress — SR-001 to SR-003 |
| A02 | Website completeness and missing pages | Pending |
| A03 | UI design, aesthetics and branding | Pending |
| A04 | UX and navigation | In progress — raw internal link graph; rendered UX pending |
| A05 | Mobile responsiveness | Pending |
| A06 | Technical SEO | In progress — source crawl completed; SR-B00-F02/F03/F06 |
| A07 | On-page SEO | In progress — source baseline and SR-B00-F01/F04/F05 |
| A08 | Google rankings and organic visibility | In progress — preliminary public search sample; controlled rankings/GSC pending |
| A09 | Keyword strategy and content gaps | In progress — F05; actual keyword mapping pending |
| A10 | Local SEO and Google Maps | In progress — SR-002; profile and map destination verification pending |
| A11 | Competitor benchmarking | In progress — public programme-page examples |
| A12 | AEO and GEO readiness | In progress — source schema inventory; eligibility and real visibility pending |
| A13 | Website speed and performance | In progress — source indicators; browser and field measurements pending |
| A14 | Accessibility | In progress — source findings F01–F03; DOM testing pending |
| A15 | Admissions and lead generation | In progress — SR-003; conversion data pending |
| A16 | Analytics and conversion tracking | Pending |
| A17 | Technology, security and privacy | Pending |
| A18 | Maintenance, reporting and accountability | In progress — F06 publication review; internal evidence pending |

## Findings register

| ID | Workstream | Finding | Severity | Evidence status | Review status | Detail |
| --- | --- | --- | --- | --- | --- | --- |
| SR-001 | A01 | NEET coaching listed on MPC–JEE programme page | High | Verified — retrieved text | Open | [Detail](findings/SR-001.md) |
| SR-B00-F01 | A07 / A14 | All 31 self-canonical pages lack native H1 headings in source | High (proposed) | Verified — source metrics | Open | [Detail](findings/SR-B00-F01.md) |
| SR-B00-F02 | A06 / A14 | Repeated HTML element IDs on all 31 canonical pages; 185 excess occurrences | Medium (proposed) | Verified — source counts; DOM scope pending | Open | [Detail](findings/SR-B00-F02.md) |
| SR-B00-F03 | A14 / A06 | Native main, header and footer elements absent on all 31 canonical pages | Medium (proposed) | Verified — native tag counts; ARIA and accessibility tree pending | Open | [Detail](findings/SR-B00-F03.md) |
| SR-B00-F04 | A07 | Missing meta descriptions on 24/31 pages, including all eight short/long exam coaching pages | High for active admissions URLs (proposed) | Verified — source metrics | Open | [Detail](findings/SR-B00-F04.md) |
| SR-B00-F05 | A07 / A09 | Five duplicate title groups affecting 10/31 canonical pages; all four short/long exam course pairs | High for active admissions URLs (proposed) | Verified — source metadata | Open | [Detail](findings/SR-B00-F05.md) |
| SR-B00-F06 | A06 / A18 | Additional homepage-copy URL is public, self-canonical and sitemap-listed with identical search metadata | High if redundant (proposed) | Verified configuration; content equivalence and indexation pending | Open | [Detail](findings/SR-B00-F06.md) |
| SR-B00-F07 | A06 / A18 | Maintenance page remains public and index-permitted | High if obsolete | Verified configuration; actual indexing pending | Open | [Detail](findings/SR-B00-F07.md) |
| SR-B00-F08 | A04 / A06 | Seven sitemap pages lack observed incoming non-self links | High for retained admissions pages; otherwise contextual | Verified within raw crawl; rendered links pending | Open | [Detail](findings/SR-B00-F08.md) |
| SR-B00-F09 | A06 | Gallery links to uppercase non-canonical Sports URL | Low to medium (proposed) | Verified URL and canonical configuration | Open | [Detail](findings/SR-B00-F09.md) |
| SR-B00-F10 | A14 / A07 | Empty image alternative text requires classification | Medium; raise for informative admission imagery | Verified counts; contextual accessibility review pending | Open | [Detail](findings/SR-B00-F10.md) |
| SR-B00-F11 | A13 | Image dimension attributes absent on 202 occurrences | Medium investigation priority | Verified source counts; actual CLS unmeasured | Open | [Detail](findings/SR-B00-F11.md) |
| SR-B00-F12 | A13 | High script element counts warrant performance investigation | Investigation; severity pending measurements | Verified source counts; performance untested | Open | [Detail](findings/SR-B00-F12.md) |
| SR-B00-F13 | A12 / A07 | Generic structured data; educational entities not detected | Medium opportunity; not a rich-result defect by itself | Verified type inventory; field-level validation pending | Open | [Detail](findings/SR-B00-F13.md) |
| SR-B00-F14 | A01 / A07 | Placeholder text in Yoga Open Graph description | Medium (proposed) | Verified metadata text; rendered body pending | Open | [Detail](findings/SR-B00-F14.md) |
| SR-B00-F15 | A06 / A18 | Elementor template entries exposed in sitemap | Investigation; priority depends on response/indexability | Verified sitemap entries; endpoint behaviour untested | Open | [Detail](findings/SR-B00-F15.md) |
| SR-002 | A01 / A10 | Contradictory Miyapur campus gender labels | High (proposed) | Verified retrieved text; correct designation pending | Open | [Detail](findings/SR-002.md) |
| SR-003 | A01 / A09 / A15 | Limited differentiated decision information in short/long JEE course copy | High for active admissions (proposed) | Verified extraction; rendered extras pending | Open | [Detail](findings/SR-003.md) |

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
