# SR-B01 — Independent validation progress
Date 2026-11-27 IST. Scope: public read-only review. This is not final audit closure.

## Performance and accessibility
Direct runtime DNS resolution of sriraama.in failed again (curl exit 6). Public PageSpeed Insights API mobile homepage and web report URLs were inaccessible through web retrieval. No Lighthouse or CrUX measurements obtained, no performance verdict. Prepared standard-library local PSI collector for 8 representative URLs x mobile and desktop (16 reports), syntax checked; live API quota/access not tested. Selected pages: homepage, contact, integrated JEE, integrated NEET, intermediate index, short-term JEE, long-term NEET, gallery. Retains aggregate scores, lab metrics, URL/origin field metrics and diagnostics; does not save embedded screenshots. If API quota denied, manually use https://pagespeed.web.dev/ and save results. Field data and lab data are distinct; TBT is not INP. Reference https://developers.google.com/speed/docs/insights/v5/about and https://developer.chrome.com/docs/crux/guides/pagespeed-insights . Need full-page rendered inspection, keyboard and accessibility tree testing and rich results validation separately. No failure inferred from tooling limitations.

## Search discovery sample
Public web retrieval, not controlled Google SERP/rank tracking; pooled results across queries on 2026-11-27. Queries: best intermediate colleges Hyderabad MPC JEE coaching Hyderabad; best junior college NEET coaching Hyderabad BiPC; best intermediate colleges Miyapur Hyderabad; short term IIT JEE coaching Hyderabad crash course; long term NEET coaching Hyderabad; site:sriraama.in "Sri Raama" Hyderabad. Sri Raama homepage and contact appeared in pooled results; cannot assign per-query positions or infer absence from Google top results. No search volume, rank, traffic or actual AI citation rates measured. Competitor pages observed:
- https://nineeducation.in/best-intermediate-colleges-with-iit-jee-coaching-hyderabad/ — intent-specific comparison/guide.
- https://nineeducation.in/top-10-junior-colleges-hyderabad-bipc-neet/ — BiPC NEET comparison content.
- https://ignite.academy/streams/test-prep/iit-jee-shortterm/ — short-term-specific title and preparation detail.
- https://vrjuniorcollege.com/courses/neet-long-term/ — dedicated long-term NEET page.
- https://invictusedu.in/programmes/neet — programme and FAQ content.
These are competitor-authored claims, not independently validated educational outcomes or rankings. Compare public content architecture; obtain controlled local SERP samples and GSC query/page data for actual visibility.

## Remaining audit gates
Rendered design/mobile and accessibility; live PSI and field data; HTML and rich-result validation; page-level content audit; local profile reconciliation; controlled search visibility and AI citation testing; admissions funnel and analytics (internal data needed); infrastructure/privacy and governance (internal evidence). No website changes or form submissions. Raw personal data not published.

## Local PSI collector attempt — 2026-11-27
User-supplied summary(1).json inspected: expected_reports=16, successful_reports=0, stopped_early=true; first request for homepage mobile returned HTTP 429. This is a Google PSI API request limit response reported by the collector, not the audited website's HTTP status or performance result. The precise quota/rate-limit cause is unknown. No Lighthouse score, CrUX data or other metric collected. Stop automatic retries. Next: run the public PageSpeed Insights UI manually for homepage mobile and desktop, or use Chrome DevTools Lighthouse locally if PSI remains unavailable. Capture report timestamps, URL, device and lab/field distinction; local Lighthouse TBT is not field INP. A13 remains pending measured validation. Do not register a site defect from the collector failure.

## Homepage PageSpeed Insights — successful manual reports
Supersedes earlier blocked performance measurement for the homepage only. Both user-supplied PDFs reviewed (mobile 11 pages, desktop 10 pages), same report timestamp 2026-11-27 14:30:26 IST. Lighthouse 13.6.0, emulated Moto G Power slow 4G / desktop custom throttling, single initial page load each. Report: https://pagespeed.web.dev/analysis/https-sriraama-in/rnqx3bcsp9bdom1vs0yai5
Mobile SHA-256 a4aa61c50ff33ea1d2442da67bc8b6d8673b428e5743ec04b8d7b0d20a9ed67a; desktop SHA-256 a2e73534a312febe040a43d3604ce50f11bd47739d35313329791f1307342204. Raw PDFs not published (contain rendered student imagery).

| Metric | Mobile | Desktop |
|---|---:|---:|
| Performance | 31 | 38 |
| Accessibility | 91 | 92 |
| Best Practices | 50 | 73 |
| SEO | 92 | 92 |
| Agentic Browsing | 1/2 | 0/2 |
| FCP seconds | 2.3 | 0.6 |
| LCP seconds | 8.9 | 1.8 |
| TBT milliseconds | 4870 | 1760 |
| CLS | 0.091 | 0.298 |
| Speed Index seconds | 15.6 | 6.3 |
| Network payload KiB | 11839 | 13874 |
| JS execution seconds | 10.2 | 5.1 |
| Main thread work seconds | 15.8 | 8.9 |
| Est. unused JS KiB | 4943 | 4946 |
| Est. unused CSS KiB | 195 | 195 |
| Est. render blocking savings ms | 1910 | 730 |
| Est. font display savings ms | 540 | 1030 |
| Est. image delivery savings KiB | 117 | 1611 |

Both reports say No Data in real-user experience section. No measured field CWV verdict or INP; TBT is a lab diagnostic. Estimated savings overlap and cannot be added. Both report 20 long tasks and missing image dimensions. Both fail contrast, discernible link names, skip link focus, main landmark and crawlable links audits; cross-reference B00-F03 for main landmark. Mobile flags one insecure request and low-resolution images; both report four third-party cookies and browser console errors. Desktop flags DevTools Issues; mobile lists that row but print view is clipped. Exact affected nodes, URLs, cookie details and errors not visible in collapsed PDFs. Gray informational security audit rows are not verified failures.
Experimental agentic browsing: mobile 1/2 (accessibility tree not well-formed); desktop 0/2 (CLS .298 and accessibility tree not well-formed). This is a browser-agent usability result, not a measure of Google/LLM indexing, AI citations, or WebMCP support. Other checks marked not applicable are not failures. Cross-reference B01-F01/F02; no separate overlapping defect count.
Registered B01-F01–F07 separately; 25 total records including earlier 18, some are investigation items rather than confirmed functional failures. Homepage measurement is now available; repeat runs and representative admissions templates remain outstanding. Next: Google Rich Results Test and expanded audit details, then additional template performance testing, rendered UI/mobile inspection, and internal-access evidence requests. No website changes.
