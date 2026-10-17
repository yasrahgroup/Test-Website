# AZAROTH Website CMS — Release 2.1.0

## Changes in 2.1.0

- Removed the navigation bar's white rounded-pill surface, backdrop blur, border and shadow. Logo, menu items and CTA are directly embedded over the page hero. The mobile *expanded menu panel* remains white for legibility.
- Added a CMS-powered **Featured Products** section to Home with image/illustration, category, summary, product overview, technology tags and deep links to product detail pages.
- Product section respects publish/draft status, provides an elegant empty state, and exposes editable heading, description and visibility in Brand & Theme.
- Added `products` to the default Home Page Builder starter layout as a Collection block; existing published custom Home layouts are not forcibly overwritten.
- Added integration and frontend regression tests for CMS product publishing and UI behaviour.
- Updated version to 2.1.0; no new runtime dependencies or database migration are required.

## Included in this package

- The supplied original burgundy/gold logo, favicon variants, and premium ivory / champagne / orange corporate UI.
- Floating navigation visually embedded into the hero, responsive mobile menu, gold-gradient CTA, animated cards, scroll reveals, and refined Glass Orb Cursor with hover behaviour.
- Dynamic Home, About, Services, Industries, Products, Blog, Case Studies, Careers, Contact, Privacy, Terms and detail-page templates.
- Live CMS with user roles, settings, colour customization, navigation manager, content publishing, category filtering, media uploads, structured page builder, draft/publish workflow and live block preview.
- Verified contact storage, recruitment application workflow with private PDF résumés, status management, audit logs, and data deletion endpoints.
- Route-level SEO metadata, sitemap.xml, robots.txt, HTTPS reverse-proxy setup, application container, backup and password-recovery utilities.
- Backward compatibility for the previous starter SQLite schema, including preserved site settings and legacy record migrations. Old media files are migrated when copied from the former project `uploads/` directory.

## Verification carried out in this environment

- `npm run check` passed for all JavaScript application files.
- `npm test`: 56 backend integration checks passed, covering authentication, roles, CSRF, CMS publishing, layouts, form persistence, private downloads, backups, data deletion, sitemap, and restart persistence.
- `npm run test:frontend`: eight main page render smoke checks plus the product/CMS/navigation assertions passed using a simulated DOM.
- Earlier starter-database migration test passed.
- CSS stylesheet parsed with no syntax errors.
- Compose YAML parsed successfully, and all referenced local website assets were checked.

## Checks that still require your hosting environment

- Building/running the Docker images (Docker CLI was unavailable here).
- Provisioning an actual HTTPS certificate for your domain.
- Human review of layout on Safari, Chrome, Firefox, mobile browsers and screen readers (local Chromium was restricted by an administrator URL block policy).
- Replacing sample company content, official photos, contact details and template legal wording.
- Configuring notification email credentials, monitoring, security review and automated off-site backup/restore verification.

This is a working full-stack application, **not a static screenshot or prototype**. Production deployment depends on completing the real-host checklist in README.md; no developer can meaningfully guarantee a deployment environment that has not been tested.
