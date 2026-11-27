# SR-B00 — Technical baseline (preliminary)
Date: 2026-11-27 IST. Scope: public website https://sriraama.in/. Not a completed crawl.

## Observations
| ID | Test | Result | Evidence status |
| --- | --- | --- | --- |
| B00-01 | CMS | WordPress strongly indicated by /wp-content/uploads/ asset path; PHP/database/theme/plugin versions not established | High confidence inference |
| B00-02 | Image delivery | sp-ao.shortpixel.ai image URLs | Verified public retrieval |
| B00-03 | Student portal | External login link to sriraama.myclassboard.com; backend integration not established | Verified link |
| B00-04 | Developer credit | Digital GYB in footer | Verified |
| B00-05 | URL inventory | 17 previously discovered candidate HTML URLs; 10 inspected, 7 gallery destinations pending | Provisional |
| B00-06 | Homepage text accessibility | Main institutional, course and campus text retrieved by web tool; raw vs rendered HTML not distinguished | Verified extraction only |
| B00-07 | Homepage headings | No H1 visible in extracted heading hierarchy; H2/H3 present | Suspected source-level defect; inspect HTML |
| B00-08 | Image descriptions | Generic labels and repeated image references in homepage extraction | Verified extraction; actual alt attributes and duplicate downloads unverified |
| B00-09 | Institutional counters | Current extraction shows zero; earlier search snapshot shows populated counters | Verified discrepancy; rendering/caching cause unverified |
| B00-10 | robots.txt | Both host variants failed through web retrieval; direct curl in audit environment failed DNS | Unverified, not proof of missing or blocked file |
| B00-11 | Sitemap | /sitemap.xml, /wp-sitemap.xml and /sitemap_index.xml retrieval unsuccessful | Unverified, not proof of missing sitemap |
| B00-12 | Raw HTML, canonical, noindex, schema | No raw HTML obtained in this environment | Pending |
| B00-13 | AI crawler policy | No verified robots policy, WAF configuration or bot logs | Pending |
| B00-14 | Search indexation | Public search returned multiple domain pages; exact Google index count not established | Partial |
| B00-15 | Rich result eligibility | No live Google Rich Results Test output obtained | Pending |

## Provisional HTML URL inventory
- https://sriraama.in/
- https://sriraama.in/about-us/
- https://sriraama.in/contact-us/
- https://sriraama.in/best-intermediate-college-in-hyderabad/
- https://sriraama.in/intermediate-mpc-with-jee-coaching-in-hyderabad/
- https://sriraama.in/intermediate-bipc-with-neet-coaching-in-hyderabad/
- https://sriraama.in/mpc/
- https://sriraama.in/long-term-course-eapcet/
- https://sriraama.in/international-studies/
- https://sriraama.in/gallery/
- https://sriraama.in/vinayaka-chavithi/
- https://sriraama.in/hanuman-chalesa/
- https://sriraama.in/freshers-party-2025/
- https://sriraama.in/farewell-party/
- https://sriraama.in/yoga/
- https://sriraama.in/wonderla/
- https://sriraama.in/Sports/

The gallery index lists seven event links. The individual paths above are candidates from the earlier discovery pass, not verified successful responses. Media/PDFs, redirects, query variants and unpublished CMS pages excluded.

## Verification sequence
1. Fetch robots.txt, declared sitemap(s), sitemap indexes and HTTP status/redirects from a network that resolves the domain. Use a polite public crawler; respect robots.
2. Crawl internal links and sitemap URLs, reconcile unique canonical indexable HTML with WordPress published page inventory and GSC Pages/Sitemaps.
3. Extract per URL HTTP status, canonical, title, meta description, robots directives, H1-H6, image alt coverage, internal links and JSON-LD/microdata/RDFa. Validate raw and rendered DOM separately.
4. Test homepage, campus/contact and programme templates with Google Rich Results Test and Schema.org Validator; do not treat non-eligible schema types as errors.
5. Review robots policies for Googlebot, Bingbot, OAI-SearchBot and other relevant search crawlers; distinguish training permissions (GPTBot, Google-Extended) from search visibility. Verify real crawler access with server logs, not spoofed user agents.
6. Test representative unbranded admissions queries across search and AI answer engines, recording date, location, source citations and methodology.

## Review questions
- What CMS, theme, builder and SEO tooling are deployed?
- How many published pages, sitemap URLs, crawlable HTML pages and Google-indexed pages exist? Can you reconcile these counts?
- Can you show the latest crawl export, GSC indexing and sitemap reports, and representative rich result tests?
- What is the documented crawler access policy, including AI search and separate training controls?

## Sources
- https://sriraama.in/ (retrieved text, 2026-11-27)
- https://sriraama.in/gallery/ (retrieved text, 2026-11-27)
- https://www.sriraama.in/wp-content/uploads/2026/02/Sriraama-Overall-Banner.jpg-1.jpeg (discovered asset reference; web fetch returned 404, requires independent retest)
- https://developers.google.com/search/docs/crawling-indexing
- https://developers.google.com/search/docs/appearance/structured-data/sd-policies
- https://developers.google.com/search/docs/appearance/structured-data/search-gallery
- https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
- https://developers.openai.com/api/docs/bots

No site changes made. No numeric HTML, SEO, schema or LLM readiness scores assigned. No confidential or personal data retained. This baseline precedes detailed defect registration; pending checks are not failures.

## Source crawl execution attempt — 2026-11-27 IST
- Direct HTTPS curl from audit runtime failed with exit 6 (could not resolve host sriraama.in). Public web retrieval of homepage succeeded independently; no site DNS outage inferred.
- Web retrieval of robots.txt, sitemap.xml, sitemap_index.xml, wp-sitemap.xml and wp-json/ remained unavailable. No absence or blockage inferred.
- Prepared downloadable standard-library Python collector sriraama_source_audit.py for execution from an independent network. SHA-256: c920f97614c83a0674a06105cf712e6ddd4baa1117f72687b38f924f68447da8.
- Syntax and synthetic parser smoke tests passed; live crawl not completed. Collector checks robots first, fails closed for ambiguous/unsupported policies, rate-limits requests, follows same-site redirects only and stops on 429/503. Bounded to 300 candidate URLs and 30 sitemaps; skips query/action paths and non-HTML assets. Output: audit.json, pages.csv, summary.json.
- Completion gate: review collector output, reconcile final URLs and canonical URLs, check remaining queues, blocked/failed endpoints and sitemap coverage. Do not infer exact published or indexed count from crawl alone.
- Independent browser rendering, HTML conformance, rich result eligibility, real search crawler logs, GSC and Core Web Vitals remain separate checks. Do not commit unsanitized output or student data to the public repository.
