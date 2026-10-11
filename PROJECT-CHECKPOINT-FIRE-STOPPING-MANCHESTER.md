# FIRE STOPPING MANCHESTER — LOCKED PROJECT CHECKPOINT
Updated: 2026-10-11

## Repository / deployment
- Repo: mleeng2026/fire-stopping-manchester
- Branch: main
- Live domain: https://firestoppingmanchesteruk.co.uk/
- Static GitHub Pages export.
- Existing location slugs must be updated in place; do not create duplicate replacement slugs.
- IMPORTANT: a GitHub commit is NOT the same as a confirmed live deployment.
- After every website edit:
  1. confirm the intended file changed on main;
  2. inspect GitHub Pages workflow for that exact commit SHA;
  3. wait until "pages build and deployment" is completed + success;
  4. where possible, visually inspect the public page;
  5. never tell Matthew "live" merely because the commit succeeded.

## Static export / hydration problem discovered
- Exported pages contained Next.js React hydration / self.__next_f scripts.
- Directly editing exported HTML while leaving old hydration data can cause the browser to reconstruct the OLD page and make new HTML appear to disappear.
- Stockport fix: remove non-JSON-LD Next/React hydration scripts from the static page being directly maintained.
- Preserve JSON-LD scripts.
- Confirm self.__next_f is absent after the fix.
- Stockport marker used: stockport-v4-static-2026-10-11.
- This is a key diagnostic if a future GitHub Pages deployment says SUCCESS but the live page still appears to show old/thin content.

## Site-wide design rules
- Preserve the existing visual system. Do not redesign from scratch.
- Header nav only: Fire Stopping / Intumescent Paint / Contact.
- Header scrolls away; not sticky/fixed.
- Header Get a Quote is secondary/subtle, not solid red.
- Mobile floating Call / Get a Quote bar removed site-wide.
- Hero secondary CTA: Get a Free Quote.
- Hero dark overlay target: about 80%.
- Photo-backed content section overlay target: about 75%.
- Use subtle genuine-photo backgrounds to break up black sections while keeping text highly readable.

## Hero centring — IMPORTANT FIX
- text-center alone does NOT centre max-width child blocks.
- For a genuinely centred hero:
  - outer hero content wrapper: mx-auto + text-center;
  - H1 with max-width: add mx-auto;
  - intro paragraph with max-width: add mx-auto;
  - CTA flex row: add justify-center (and items-center where useful);
  - breadcrumb flex: justify-center;
  - badge can remain inline-flex inside centred parent.
- Stockport mistake: first pass only added text-center, so the H1/paragraph/buttons remained physically left-positioned.
- Correct Stockport fix used:
  - H1: mx-auto mb-5 max-w-4xl ...
  - paragraph: mx-auto mb-8 max-w-2xl ...
  - CTA row: flex flex-col items-center justify-center ... sm:flex-row ...
- When Matthew says "centred", visually centre the entire content block, not merely its text alignment.

## V4 Mega Mega location-page rules
- BOFU first: speak to someone who needs a quote, remedials, handover work, survey defects closed, penetrations sealed, or steel protected.
- AEO: clear question/answer headings and concise direct answers backed by useful detail.
- Natural UK working English. No AI-ish padding or corporate waffle.
- Deep local substance. Pages must NOT feel like town-name-swapped doorway/scaled pages.
- Use real local building mix, commercial/industrial areas, sub-areas and regeneration context where relevant.
- Never invent completed local projects.
- Real enquiries may be used as examples, but explicitly describe them as enquiries / enquiry types and never imply completed work.
- Internal-link naturally to relevant service pages and parent Greater Manchester hub.
- One H1. Clean H2/H3 hierarchy.
- Visible FAQs must match FAQ schema.
- Keep page-specific JSON-LD clean: LocalBusiness, WebSite, WebPage, Service, ImageObject where appropriate, BreadcrumbList, FAQPage.

## Location image rule — LOCKED
- Use genuine fire stopping / intumescent project-type photos.
- Prefer a different genuine photo for each placement.
- Never add/remove/generate content inside a genuine project photograph without Matthew's approval.
- Convert web images to good-quality WebP where practical.
- Avoid over-compressing full-width/background images.
- Filenames MUST contain:
  service + MAIN LOCATION + useful sub-location/descriptor.
- For Stockport, EVERY Stockport-page image filename must contain "stockport", even if Bredbury/Cheadle/Hazel Grove/Reddish/etc is also present.
- Example: fire-stopping-stockport-bredbury-cable-tray-penetrations.webp
- A renamed image does NOT claim the photographed job occurred in that location.
- 4–6 relevant photos per substantial location page is a good target.
- STRICT filename formula for location pages: SERVICE + MAIN TARGET LOCATION + SUB-LOCATION + USEFUL DESCRIPTOR.
- The main target location must NEVER be replaced by the sub-location. Example: duct-penetration-fire-stopping-bolton-middlebrook-commercial-services.jpg.
- STRICT PHOTO SOURCE RULE: use genuine user/client project photos already supplied in Drive/repo only. NEVER generate AI project/site photographs for this website unless Matthew explicitly reverses this rule.
- Do not put visible defensive captions under genuine project photos. Avoid false location claims in the copy instead.
- Use additional genuine photos as subtle ~75% dark section backgrounds when a page looks visually bland.

## Stockport status
- Existing slug: /fire-stopping-stockport/
- File: fire-stopping-stockport/index.html
- V4 substantive content added with 9 major Stockport sections and six local-renamed genuine project images.
- Stockport local depth includes town centre, Underbanks, Edgeley, Bredbury, Reddish, Cheadle, Bird Hall Lane, Hazel Grove, Bramhall, Heaton Moor/Chapel, Marple where contextually useful.
- Real enquiry examples can include Stockport steel/listed-building enquiry and Stockport soil-stack/riser/fire-collar enquiry, plus wider Greater Manchester enquiry patterns, clearly labelled as enquiries.
- Relevant internal links include cable tray, service penetration, pipe penetration, duct penetration, compartmentation remedials, fire batt & mastic, commercial fire stopping, intumescent paint, Greater Manchester hub and contact.
- Hydration/static fix commit: 528bf363a2c7f35407aad61cb1df603453cfa463
- Proper hero-centering fix commit: e2d54662a5b7b99d3c999930908dde2d262ab798

## Salford / Trafford checkpoint
- Salford + Trafford were rewritten to V3/V4-style substantial local standard.
- Areas + FAQs collapsed into accordions where already implemented.
- Important BOFU sections stay open.
- FAQ schema matches visible FAQs.
- Trafford "Fire stopping contractors in Trafford" uses Lowry/Trafford construction background with approx 75% dark overlay.
- Full-width background image quality matters: do not upload a tiny over-compressed WebP and call it high resolution.

## Forms
- Homepage uses Formspree.
- Contact page uses same Formspree endpoint.
- File-upload field added under project details.

## Communication / execution rule
- Do the requested website task rather than repeatedly planning it.
- If blocked by GitHub/tooling, say exactly what is blocked immediately.
- Do not claim an image/file/page is live until deployment is confirmed.
- Do not claim visual verification if it was not actually visually checked.
- Preserve context from this checkpoint before editing future Manchester pages.
