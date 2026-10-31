# SEO Report — Muhammad Haris Afzal portfolio
Checked: 2026-10-31. Live site: https://0git00.github.io/Email-Marketing/

## 1. Critical finding: three different URLs
| Source | Canonical/URL used |
|---|---|
| Live site (as fetched) | `/Emil-Marketing/` — returns an error, so the live canonical points at a dead page |
| Uploaded index.html (before) | `/MuhammadHarisAfzal/` — not the live path |
| Real live path | `/Email-Marketing/` |
All 13 occurrences (canonical, og:url, og:image, twitter:image, JSON-LD) now use `https://0git00.github.io/Email-Marketing/`.
This is the most important fix: a canonical pointing at a missing page tells search engines to ignore the real one.

## 2. What was changed in index.html (only head/meta; body and design untouched)
- Canonical, og:url, og:image, twitter:image, JSON-LD ids/urls corrected (see above)
- Title: `Muhammad Haris Afzal | Email Marketing Expert & Freelancer` (58 chars)
- Meta description rewritten (145 chars) to include freelance, Klaviyo, Mailchimp, HubSpot, Brevo
- OG/Twitter title and description aligned
- Removed `meta keywords` (ignored by Google) and a single-language self `hreflang` (no alternate versions exist)
- Person JSON-LD description aligned with the title
Added files: robots.txt, sitemap.xml, site.webmanifest.

## 3. Limitations you must know about
1. **robots.txt on a project subpath is ignored.** Crawlers read robots.txt only at the host root (`https://0git00.github.io/robots.txt`). That needs a repository named exactly `0git00.github.io`. The file is harmless here but does nothing until then. sitemap.xml works fine at the subpath.
2. **Files referenced but not uploaded** (could not verify they exist): `assets/og-image.jpg`, `assets/profile.jpg`, `assets/apple-touch-icon.png`. If missing, social previews and the schema image break. Upload them or tell me and I will remove the references.
3. **Keyword metrics are UNKNOWN.** I have no access to a keyword tool, and web search does not return volume or difficulty. The CSV marks every metric UNKNOWN instead of inventing numbers. Free ways to fill it in: Google Keyword Planner (needs a free Google Ads account), Google Trends, Bing Webmaster keyword research, AnswerThePublic, Ubersuggest free tier.
4. **No Lighthouse, W3C validator, or Rich Results Test was run** (no network in my sandbox). Run those yourself after deploy.

## 4. Realistic ranking picture (from one live SERP check)
For "hire freelance email marketing specialist" the results were Toptal, MarketerHire, FreeUp, Upwork, Fiverr, Contra, Freelancer.com, Klaviyo's own blog and agency pages. A new github.io subpath site is very unlikely to reach page one for the generic head terms. Realistic order of winnability:
1. Your own name ("Muhammad Haris Afzal email marketing") — branded, should be achievable.
2. Narrow long-tail terms backed by genuine pages (deliverability fix, Klaviyo flow rebuild, segmentation).
3. Head terms ("email marketing expert/specialist/services/freelancer") — long-term, and not promised.
Only 1 competitor-set search was run, so this is not the 10-competitor audit requested; a proper one needs SERP tooling.

## 4b. Content issues on the live site worth your review (not edited)
These are your claims, so I left them, but they affect trust and consistency:
- Hero says **25%+ avg open rate**, Results section says **48%** — contradictory.
- Hero **4.8x ROI**, three case-study percentages, and three named testimonials (Sarah M., Daniel R., Priya K.). If any are placeholders or unverifiable, remove or replace them with real, permissioned ones; fabricated testimonials risk client trust and platform rules (and Google's reviews guidance).
- Every service shows "From $15", which looks like a template default.
- Single page only: all keyword targets compete on one URL. Add pages only where you have genuine content.

## 5. Content plan (only pages you can back with real experience)
| Page | Target | Intent |
|---|---|---|
| /services/email-deliverability/ | email deliverability consultant | commercial |
| /services/klaviyo-flows/ | klaviyo email marketing expert | commercial |
| /blog/email-list-segmentation/ | email list segmentation | informational |
| /blog/spf-dkim-dmarc-setup/ | SPF DKIM DMARC setup for email | informational |
Word counts: size to the topic; no filler. Link each back to the homepage Contact section.

## 6. Discovery without Search Console
- Sitemap is declared via `<link rel="sitemap">` and robots.txt (root only, see above).
- Bing Webmaster Tools (separate from Google) accepts sitemap submission and IndexNow.
- Public links to the site from LinkedIn (already in sameAs), Fiverr profile, GitHub profile README, Instagram bio.
- Google may discover the site from those links; nothing guarantees indexing or ranking.

## 7. Legitimate backlink opportunities
LinkedIn profile/featured link, Fiverr profile website field, GitHub profile + repo description, Instagram bio, Klaviyo/Mailchimp partner or expert directories (only if you qualify), Contra/Behance-style portfolio profiles, genuine guest posts or community answers (Reddit r/emailmarketing, Indie Hackers) without link spam.

## 8. Validation actually performed
- JSON-LD (2 blocks) parses; types WebSite, Person, ProfessionalService, FAQPage
- sitemap.xml well-formed; manifest valid JSON
- No duplicate IDs; all in-page anchors resolve; one H1; tags balanced
- All 4 inline JS blocks pass `node --check`
- Title 58 chars, description 145 chars
Not performed: rendering, Lighthouse, W3C validator, live link checks, image weight audit.

## 9. Deploy
1. Replace `index.html` in the `Email-Marketing` repo with `site/index.html`.
2. Add `sitemap.xml`, `site.webmanifest` (and `robots.txt`, optionally, see §3.1) in the same folder.
3. Confirm `assets/og-image.jpg`, `assets/profile.jpg`, `assets/apple-touch-icon.png` exist.
4. Commit, wait for Pages to rebuild, open `/sitemap.xml` and view-source to confirm the canonical.
Keep `backup/index.original.html` for rollback.
