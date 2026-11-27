# SR-B11 — Final public audit reconciliation for Presentation 1

Date: 2026-11-27 IST. User-directed scope closure: conclude the independent public website audit from available evidence, and carry unavailable or internal verification to management review. This is completion of the agreed evidence-gathering scope, not certification of site quality, remediation, or closure of individual findings. No new live crawl was performed in this reconciliation.

## Inventory and coverage
All 48 individual finding documents and 11 preceding baseline reports (B00–B10) were reopened and reviewed. The master contains 48 distinct references: 15 B00 technical, 7 B01 Lighthouse, 26 SR-001–026 editorial, campus, commercial, UX and infrastructure observations. All findings remain open for response/remediation. B09 ROI report exists but was not linked in the prior master; restore its link. No new findings added or deleted. Historic observations and later corroboration are preserved; use the latest evidence when discussing each issue.

31 self-canonical public HTML pages in the bounded source crawl; 35 candidate requests final HTTP 200, 32 distinct final HTML URLs including uppercase Sports variant. 24 pages returned public text in the editorial pass B08; Success subsequently retrieved from user's open tab (B10), bringing cumulative successful page text retrieval to 25/31. Six remaining body-text gaps: /bipc/, /sports/, /pooja/, /blog/, /home-copy/, /home-2/. All six returned HTTP 200 in original crawl; later extraction unavailable is not site failure. Full rendered coverage of all pages not established. Homepage mobile and desktop Lighthouse reports were user-supplied on 2026-11-27; no real-user data.

## Management presentation evidence groups
Each finding assigned once for discussion; overlapping observations cross-reference one another and should not be added as independent failures.
| Group | IDs | Count | Management discussion |
| --- | --- | ---: | --- |
| Technical SEO, indexability and publication | B00-F01, F04, F05, F06, F07, F08, F09, F15; B01-F03; SR-025 | 10 | Source heading/metadata, duplicate/public URLs, links, sitemap, and About intent; show publication QA and URL inspection |
| Academic accuracy and editorial trust | B00-F14; SR-001, 004, 005, 014, 015, 016, 022, 023, 024, 026 | 11 | Correct programme wording, placeholders, counters, substantiated claims, exam terminology, dated materials and media provenance |
| Campus and local discovery | SR-002, 006, 011, 012, 013 | 5 | Approved campus identity, shared Maps link, address/phone reconciliation, useful location pages and reputation |
| Performance and infrastructure | B00-F11, F12; B01-F01; SR-021 | 4 | Measured homepage lab results, image dimensions, script workload, cache strategy; no proven causal attribution |
| Accessibility and user interface | B00-F02, F03, F10; B01-F02, F07; SR-017, 018, 019 | 8 | Source identifiers and landmarks, contextual image labels, automated accessibility flags, homepage hierarchy and mobile controls; no blanket WCAG verdict |
| Admissions, content discovery and structured data | B00-F13; SR-003, 007, 008, 009, 010 | 6 | Programme differentiation, enquiry disclosure, machine-readable content, dedicated destinations and parent guides |
| Security, privacy and runtime quality | B01-F04, F05, F06; SR-020 | 4 | Investigate insecure request, errors, cookies and header configuration privately; no breach or legal finding |
| Total | | 48 | Findings and investigation items, not 48 proven failures |

## Strongest measured evidence
- 31/31 no native H1 in source; 24/31 missing meta description (including all eight short/long-term coaching URLs); 10/31 duplicate titles; all four duration pairs also share exact OG descriptions. 185 excess ID occurrences (not distinct IDs); 7/31 no incoming non-self raw link in bounded graph.
- Public /home-copy/ and /home-2/ both 200, self-canonical, index-permitted and sitemap-listed; purpose and actual indexing require demonstration.
- Homepage Lighthouse mobile/desktop 31/38 performance; LCP 8.9/1.8 seconds; TBT 4870/1760 ms; CLS 0.091/0.298; payload 11839/13874 KiB; estimated unused JS 4943/4946 KiB. One run/device, no field data, no additive savings. SEO score 92 on both is basic homepage check, not website-wide SEO outcome. Experimental agentic browsing 1/2 and 0/2 is not AI citation visibility.
- SR-001 unexplained NEET feature on MPC/JEE page; SR-004 engineering introduction on both NEET pages; SR-022 incorrect BITSAT institution name; B00-F14 placeholder text in Yoga metadata and retrieved body; SR-002 conflicting gender labels; SR-011 same Maps heading link for two distinct addresses; SR-024 historical Success materials confirmed by browser tab, with newer 2025-named PDF separately discovered, not inspected.
- No dedicated campus or admissions destination in bounded URL inventory; competitor content examples support improvement opportunity, not measured rankings or admissions superiority.
- Positive controls: all 35 candidate requests final 200, canonical and sitemap declarations for 31 pages, homepage aliases redirect to HTTPS non-www, robots permits search crawlers, 31 parseable JSON-LD blocks, programme and contact content retrievable, 46 form elements and five official social links. These do not establish successful form processing or complete indexation.

## Interpretation guardrails and reconciled updates
B00-F03 native landmark absence corroborated by homepage automated missing-main finding B01-F02; no claim all pages lack effective ARIA equivalents. B00-F11 and F12 source observations corroborated by homepage performance measurements, not proof they caused specific shifts or delays. B00-F12 counts script elements with nonempty src, not actual requests; F06 script counts interpreted accordingly. B00-F14 later public text confirms body placeholder. B00-F05 exact OG pairs included, not extra findings. SR-024 browser corroboration supersedes source-only status; brochure contents and latest approved version still unverified. SR-002 and SR-011 distinct label versus link observations. All 48 records remain open, priority ratings provisional. No arbitrary overall score, precise Google ranks, causal revenue loss, academic outcomes, vulnerability exploitability, WCAG conformance or privacy violation inferred.

## Evidence requests for management review (not additional independent audit gates)
| Evidence owner/topic | Request | Decision supported |
| --- | --- | --- |
| SEO team | GSC 16 months query/page/indexing exports, target keyword map, local/device rank tracking, backlink and content logs, canonical inspection | Actual search visibility, SEO deliverables |
| Web team | CMS inventory, approved metadata/heading checklist, source/rendered crawl, sitemap disposition, full-page device QA, actual Lighthouse diagnostics and repeat tests, rich-results/schema results | Publication quality, performance, navigation and accessibility |
| Academic and campus leads | Approved programme/campus master, current dates and fees, official exam references, ranking substantiation, brochure approvals and university partnerships | Factual accuracy and parent trust |
| Local/social team | Eligible verified profiles and ownership, correct map pins/phone routing, public posting and review process, GBP performance | Local presence and brand governance |
| Marketing/admissions | GA4/GTM, campaign reports, lead routing and deduplication, qualified leads and confirmed admissions by channel/campus/programme, actual spend/invoices and cohort attribution | Marketing effectiveness and ROI; B06/B09 |
| Infrastructure/privacy | Institution-controlled domain/hosting/analytics access, current dependency inventory, authorized security review, consent and data flow, backup/restore evidence, incident and uptime history | Operational continuity and data protection |
| Contract manager | Signed scope, monthly deliverables, approved budgets, payments, reports and acceptance criteria | Contractual responsibility; no breach finding without records |

Do not request passwords or publish identifiable student/parent data, raw financial files or security-sensitive details. Use read-only authorized demonstration and aggregate reports. Unavailable checks: direct Google rankings and detailed Ahrefs SERP plan, actual platform AI citations, executed schema/rich-results output, detailed social activity, full-page interaction and manual accessibility, additional templates' speed, actual crawler logs, actual form delivery and authenticated controls. Carry these to the team review; they are not reasons to delay presentation and not counted as failures. Public website and pages audit complete within user-approved scope; internal assurance and remediation remain outstanding.

## Next deliverable
Presentation 1: factual public observations and independent evidence; key cross-questions; team evidence requests; agreed action owner, due date and retest criteria. All 48 references available as appendix. Presentation 2 remains a separate private management proposal; no private commercial strategy included here.

Master IDs reconciled: SR-001, SR-B00-F01, SR-B00-F02, SR-B00-F03, SR-B00-F04, SR-B00-F05, SR-B00-F06, SR-B00-F07, SR-B00-F08, SR-B00-F09, SR-B00-F10, SR-B00-F11, SR-B00-F12, SR-B00-F13, SR-B00-F14, SR-B00-F15, SR-002, SR-003, SR-B01-F01, SR-B01-F02, SR-B01-F03, SR-B01-F04, SR-B01-F05, SR-B01-F06, SR-B01-F07, SR-004, SR-005, SR-006, SR-007, SR-008, SR-009, SR-010, SR-011, SR-012, SR-013, SR-014, SR-015, SR-016, SR-017, SR-018, SR-019, SR-020, SR-021, SR-022, SR-023, SR-024, SR-025, SR-026.
