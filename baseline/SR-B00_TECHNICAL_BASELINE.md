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

## Local source crawl — evidence reconciliation (2026-11-27 14:08 IST)
Mac collector succeeded. This section supersedes earlier network-blocked observations.
Inputs reviewed: audit.json (SHA-256 f1ce16437a0a19dc260d0859814c17716f7f29673c74e36378cbf5f1ad0a137a), pages.csv (65ad0baeb21ae70229254c4e99d03e862d6a8446a87a2db6726ab58a3d937b06), summary.json (f574558c2a00bedd92e89f31dd853177dcb62f798fdb4715a082a11e51a7b78c). Summary matches JSON; 35 CSV rows reconcile with JSON in URL, final URL, status, H1 count and meta description. Raw files not published.
- 54 requests; 35 candidate HTML requests, all final HTTP 200; 32 distinct final URLs; 31 self-canonical pages (all present in page sitemap); uppercase /Sports/ returns 200 with canonical /sports/. Three homepage aliases redirect via 301 to HTTPS non-www; HTTP www takes two hops. No remaining candidates or sitemap queue; no rate-limit halt.
- Sitemap index returns 200 and lists page-sitemap.xml (31 URLs) and elementskit_template-sitemap.xml (2 query URLs skipped by collector). /sitemap.xml and /wp-sitemap.xml redirect to index. Sitemap XML noindex, follow is not a page-indexability defect.
- Robots returns 200 on four origins; wildcard empty Disallow and sitemap index declaration. Preliminary root policy allows all tested search and training agents. Real bot-specific WAF and logs untested.
- Source advertises WordPress 7.1.5 and Elementor 4.3.2; response headers report PHP 8.3.37 and LiteSpeed. Treat as reported versions, not authenticated installation/version or vulnerability proof. Yoast robots block, WordPress and Elementor asset signals, Autoptimize, ElementsKit Lite, Essential Addons for Elementor Lite, Bluehost WordPress plugin, CF7 Math CAPTCHA and horizontal scrolling announcements detected. Hosting provider and theme unconfirmed.
- Denominator: 31 distinct self-canonical pages; all report index/follow, one title, viewport, lang, one parseable JSON-LD block, no missing alt attributes. No page-level X-Robots-Tag recorded. All lack H1 and native main/header/footer tags; all contain duplicate IDs (5–7 excess ID occurrences per page, not distinct repeated ID values). Native tag absence does not establish absence of equivalent ARIA landmarks.
- 24/31 lack meta descriptions; 10/31 share titles across five groups: homepage/home-copy; short/long JEE; short/long NEET; short/long EAPCET; short/long BITSAT. Home-copy duplicates homepage title and description but has different raw response hash; content equivalence untested.
- 529 img element occurrences; 331 empty alt, none missing alt, 202 missing dimension attributes. Decorative images can legitimately have empty alt; responsive CSS can reserve space; manual checks required.
- 47–57 script elements with nonempty src per page (not network requests or inline scripts); homepage 252689 source bytes; home-copy 256932; range 92552–256932. Not transfer sizes or speed scores.
- All 31 have identical detected JSON-LD type sets: BreadcrumbList, EntryPoint, ImageObject, ListItem, Organization, PropertyValueSpecification, ReadAction, SearchAction, WebPage, WebSite. No Course or specific educational/campus entity type detected. Type inventory and parseability do not prove Google eligibility, entity accuracy or LLM citation.
- /home-2/ title Coming Soon Page - Sriraama; OG description announces maintenance; self-canonical, sitemap-listed and index/follow. /home-copy/ similarly self-canonical and sitemap-listed. Seven sitemap pages lack incoming non-self links when canonical target of /Sports/ is accounted for: /home-copy/, /pooja/, /blog/, /bipc/, /home-2/, /success/, /mpc/. Scope only raw discovered internal anchors; not definitive orphan status.
- /yoga/ OG description contains Lorem ipsum placeholder text. /success/ OG description refers to IPE Results-2022; three linked PDF filenames refer to 2022/2023. Currency of information and PDF content require review.
- Missing native H1 finding registered separately as SR-B00-F01; remaining findings are queued for one-at-a-time review, not assigned final severity.
Remaining checks: actual CMS and GSC counts, query template response behaviour, full source conformance, rendered DOM and accessibility, schema fields and Google Rich Results Test, lab/field performance, real crawler logs and actual AI search visibility. No live form submissions, intrusive tests or site modifications.

## Duplicate-ID metric clarification
Collector implementation inspected: duplicate_id_count = sum(v-1 for v in p.ids.values() if v>1). 16 canonical pages have 5 excess occurrences and 15 have 7 (185 total). Exact values, affected references and same-tree scope require follow-up. See findings/SR-B00-F02.md.

## Raw-source findings registration
All queued F01–F15 now have individual records in findings/ and are included in MASTER_AUDIT_CHECKLIST.md, alongside SR-001 (16 total). Raw-source review of the queued observations is complete within collector scope. F10/F11/F12/F13/F15 are contextual opportunities or investigation items, not confirmed functional failures. Remaining browser, rich-result, performance, actual indexing and crawler checks stay open. No raw files published. Further editorial observations (About title/description intent mismatch, generic OG copy across coaching pages, older results and leaflet references) are candidates for later content audit, not counted here.

## Script metric clarification (Phase 07)
Reopened collector implementation: script_count counts only script elements with nonempty src, excludes inline-only scripts and inline JSON-LD. This corrects earlier generic script-count descriptions across the register, including F06 and F12. Numeric counts (1494 total) and independent Lighthouse metrics unchanged. See SR-B06.
