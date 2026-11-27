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
