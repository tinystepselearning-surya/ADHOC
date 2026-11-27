# SR-B06 — Analytics and admissions conversion assurance
Date 2026-11-27 IST. Public read-only assessment and internal evidence plan. No new confirmed defect registered; cross-reference SR-007, SR-009 and B01-F06. This report is not a finding of missing analytics.

## Evidence
Reopened audit.json (SHA-256 f1ce16437a0a19dc260d0859814c17716f7f29673c74e36378cbf5f1ad0a137a) and sriraama_source_audit.py. Deduplicated by final URL and retained canonical=[final_url]. 31 pages; 46 form elements, 16 pages with one and 15 with two. All eight short/long entrance course pages have two, as do homepage/contact/integrated JEE/integrated NEET. Form occurrences are not unique lead forms. Collector does not preserve form actions, field definitions, individual script URLs, inline tracking code or network requests. All 31 expose CF7 Math CAPTCHA asset slug; this does not prove form delivery or CRM integration. Prior public retrieval identifies MyClassboard portal link, not a verified CRM connection. Both homepage PSI reports flagged four third-party cookies; exact purpose unknown. Direct curl recheck failed DNS (exit 6) in audit environment. GA4, GTM, Ads, Meta, Clarity, server-side or offline tracking and consent are unverified, not absent.

## Measurement contract (proposed audit criteria, not current implementation)
| Stage | Evidence / counting rule |
|---|---|
| Traffic | GA4 sessions by landing page, session source/medium, campaign and device; reconcile GSC clicks separately, not equal to sessions |
| Contact intent | Phone/WhatsApp clicks tracked separately from successful enquiries; click is not a conversation |
| Enquiry | Server-accepted form or verified incoming enquiry, unique first-party lead after deduplication; no counting failed CAPTCHA, refresh, double click |
| Qualified enquiry | Agreed eligibility and genuine intent, first-party CRM status; preserve unknown/unqualified reason |
| Counselling / visit | Distinct scheduled and completed events; agreed definition |
| Application | Unique application for approved course/campus/cycle |
| Confirmed admission | Institution-approved definition (e.g. accepted enrolment with required payment), distinct student/admission; handle cancellation/refund |
Google GA4 recommended events include generate_lead, qualify_lead and close_convert_lead: https://developers.google.com/analytics/devguides/collection/ga4/reference/events . These are examples, not prescribed implementation and not verified deployed. Reconcile first-party CRM and admission ledger with aggregate reporting; never equate event counts with unique people. Allow unattributed admissions; disclose attribution model/window, multi-touch, cross-device, offline conversion lag and deduplication. Cohort conversions by enquiry date with sufficient maturation; separately report calendar-period confirmed admissions.

## Evidence requests
- Institution-owned account/roles for GA4, GTM, Ads, Meta, CRM, GSC; demonstrate live read-only, do not share passwords.
- GA4 last 12 months monthly traffic acquisition, landing page, events/key events, device, data streams and destinations; report completeness, timezone, filters and retention.
- GTM published version, tag/trigger inventory, duplicate tag detection, consent state and sanitized event parameters; Tag Assistant https://tagassistant.google.com/ (guide https://support.google.com/analytics/answer/15756111).
- CRM aggregate lead counts by acquisition channel/programme/campus, duplicates, valid/qualified, response time, visits, applications, admissions and unknown source; campaign IDs/UTM convention and attribution policy. Show lead routing and failed delivery monitoring.
- Reconcile platform spend, invoices, CRM and admissions ledger by period and cohort, avoiding double attribution across ad platforms; compare approved costs and outcomes. Report missing data as unknown, not zero.
- Privacy: inspect sanitized event URLs, payloads, cookies and consent state without collecting raw identifiers. Ordinary GA4 events must not contain names, emails, phone numbers, child identifiers or free text with personal information; review separately authorized supported integrations and their requirements. Reference https://support.google.com/analytics/answer/6366371 . No claim of observed PII leakage.
## Demonstration / closure
Public browser Tag Assistant on homepage, contact, JEE, NEET: observe detected tags and page-load events; check consent and duplicate firing without form submissions or advertising clicks. Presence of a tag does not establish correct destination or lead tracking. Team-authorized staging/synthetic test: accepted lead exactly once; invalid CAPTCHA, validation failure, retry and duplicate submit don't create false conversions; verify server acceptance, CRM assignment, consent-safe attribution and admission status. No real student/parent data or private credentials in public repo. A15/A16 remain open pending internal verification; use this audit as meeting evidence request, not confirmed defects.

## Correction to earlier source terminology
Collector's script_count is len(p.scripts), populated only for script tags with nonempty src. 1494 across 31 pages, 47–57/page, counts source-referenced script elements, not all inline scripts or JSON-LD blocks without src. It remains neither actual network request count nor unique resources. See corrected B00-F12. Lighthouse lab performance measurements unaffected.
