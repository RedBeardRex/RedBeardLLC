# Red Beard Studios LLC Corporate Landing Page

Corporate website for **Red Beard Studios LLC**, a Montana-based company operating media, software, ecommerce, and digital product businesses.

Canonical public domain: **https://red-beard.com**

Public contact email: **info@red-beard.com**

Public mailing address:

1106 W. Park Street Suite 20 # 142  
Livingston, MT 59047

## Project Purpose

This site is intentionally small. It serves as:

- the public corporate home for Red Beard Studios LLC;
- proof of legitimacy for customers, partners, payment providers, OAuth providers, and other services;
- the canonical parent-company identity for approved Red Beard Studios LLC products and brands;
- a stable location for company contact and legal information.

It is not intended to be a large marketing site or creator landing page.

## Approved Public Brands / Projects

The following public brands/projects are approved for the corporate home page and should be presented as clickable destinations:

- **The Den of Tools** — https://www.youtube.com/@denoftools
- **3D Print Rancher** — https://www.youtube.com/@3dprintrancher
- **Print Ranch Manager** — https://www.printranchmanager.com
- **Coach Jeff King** — https://www.youtube.com/@CoachJeffKing
- **CamoBot** — https://camobot.com

Do not add experimental, private, unreleased, or other Red Beard Studios LLC projects unless Jeff explicitly approves them for public listing.

### Brand-link behavior

- Each approved brand name/card should link to its approved destination above.
- Use normal accessible anchor elements with descriptive text and visible keyboard focus.
- External destinations may open in the same tab unless there is a strong usability reason to do otherwise; do not add intrusive interstitials.
- Do not add affiliate parameters, tracking parameters, analytics, or redirects.
- Verify every destination before deployment and report any broken or unexpected destination rather than silently substituting another URL.

## Hosting and Infrastructure

Hosting: **GitHub Pages**

Requirements:

- $0/month hosting
- static site only
- custom domain support
- HTTPS
- no database
- no CMS
- no WordPress
- no unnecessary JavaScript frameworks
- no analytics or tracking by default
- easy for Codex to maintain directly through GitHub
- DNS remains managed at the current registrar and points to GitHub Pages

Production DNS is already configured and must not be changed during normal site-content work.

## Site Architecture

```text
/
├── index.html
├── privacy.html
├── terms.html
├── accessibility.html
├── css/
│   └── styles.css
├── assets/
│   └── ...
├── CNAME
└── README.md
```

A separate Brands page is not required. Approved brands can be presented cleanly on the home page.

### Home Page

Include:

- Red Beard Studios LLC corporate identity
- concise positioning statement: a Montana-based media, software, ecommerce, and digital products company
- brief About section
- approved public brands/projects with working links
- public contact and business information
- links to legal/trust pages
- copyright notice

### Legal / Trust

Include:

- Privacy Policy
- Terms of Use
- Accessibility Statement
- Contact information
- Copyright notice

Add an affiliate disclosure only if the Red Beard Studios LLC corporate site itself contains affiliate links.

Do not add GDPR, CCPA, cookie-consent, or similar compliance UI unless the site's actual behavior or legal requirements make it necessary.

## Design Direction

The site should feel:

- professional
- understated
- trustworthy
- modern
- Montana-based without cowboy clichés
- more like a small holding/operating company than a creator landing page

Avoid:

- fake corporate stock-photo aesthetics
- excessive animation
- overly AI-looking design
- startup jargon
- unnecessary sections

## Identity / Logo

Jeff confirmed the official public identity is **Red Beard Studios LLC**. This supersedes the earlier working identity **Red Beard LLC** for public-facing site branding.

Jeff supplied approved production logo artwork, now preserved unchanged in `assets/brand/originals/`, including:

- primary stacked logo
- standalone RB monogram
- horizontal lockup
- one-color black version

Implemented web treatment:

- horizontal lockup in the site header
- standalone RB monogram for favicon/app-icon use
- text fallback retained for accessibility and failure cases

Do not invent, redraw, trace, or approximate the logo. If the approved files are not available to Codex, retain the current text identity and report the asset dependency.

Approved palette from the supplied brand sheets:

- Charcoal Black: `#111111`
- Deep Red: `#8E1F1F`
- Warm Ivory: `#F5F2ED`
- Warm Gray: `#B8B0A6`

Brand direction remains premium, understated, and modern.

## Technical Standards

- semantic HTML5
- responsive CSS
- keyboard accessibility
- visible focus states
- proper labels and document landmarks
- reasonable WCAG 2.2 AA practices
- sufficient text/background contrast
- minimal or zero JavaScript unless a concrete requirement emerges
- no tracking scripts by default
- no third-party dependencies unless justified
- fast loading and easy maintenance
- sensible title, description, canonical, Open Graph, and other basic metadata

## Development Roles

**JEFF** — Product Owner  
Approves public identity, content, brands, major scope decisions, and production launch.

**CHATGPT** — Senior Product Architect / Project Manager  
Defines architecture and requirements, reviews Codex work, manages scope and project handshake, and hands implementation tasks to Codex.

**CODEX** — Implementation Engineer  
Implements approved work in the repository, tests it, documents completed actions, and returns ownership through the handshake.

## Implementation History

### RBLP-001 — V1 site

Implemented September 11, 2026; initial implementation commit: `7c8f921`.

- Four static pages: home, privacy, terms, accessibility.
- Shared responsive CSS and CNAME.
- Semantic structure, skip link, visible keyboard focus, metadata and canonical URLs.
- No JavaScript framework, analytics, trackers, forms, remote fonts, or other third-party asset dependencies.
- Initial responsive, link, keyboard and contrast checks passed.

### RBLP-002 — Production launch

Production is **LIVE** at **https://red-beard.com**.

Launch milestones:

- GitHub Pages enabled from `main` at repository root.
- Old GoDaddy YouTube forwarding removed.
- Apex DNS set to GitHub Pages A records:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- `www` CNAME set to `redbeardrex.github.io`.
- Existing nameservers, MX, TXT, email, verification, unrelated subdomain, billing, ownership, privacy, renewal and security settings were preserved.
- GitHub custom-domain certificate issued for apex and `www`.
- HTTPS enforcement enabled.
- Final company-name correction to **Red Beard Studios LLC** implemented in commit `e23fb2c`.
- Deployment `34669826392` built successfully.
- Apex and `www`, HTTP and HTTPS, required pages and stylesheet were verified with valid TLS and correct redirects/path preservation.
- Static/link, responsive, keyboard and contrast checks passed after launch.

### Production protection

The GoDaddy/DNS/HTTPS launch configuration is complete and must not be repeated or modified during normal branding/content work. Any future DNS, nameserver, certificate, email-record, forwarding, registrar-account or GitHub Pages hosting change requires a new explicit authorization from Jeff through the handshake.

## Current Branding Status

- Public company identity: **Red Beard Studios LLC** — deployed.
- Domain: **https://red-beard.com** — live with HTTPS enforced.
- Approved logo artwork: identified and imported for RBLP-004; Image 3 is the horizontal lockup and Image 2 is the color RB monogram.
- Header identity: approved horizontal lockup with native alt-text failure fallback and an accessible home-link name.
- Icons: approved RB monogram in ICO and PNG sizes; no artwork recoloring or redrawing.
- Approved brand destinations: now supplied and locked above.
- Approved public brand list now contains five entries, including **CamoBot**; all five entries are deployed on the home page.

## RBLP-003 Implementation and Verification

Implementation commit: `8c4826b` (pushed to main). The home page now lists all four approved brands as normal same-tab anchor links using the exact approved URLs. Links occupy the brand row width, are underlined, retain visible keyboard focus, and have a restrained hover color. No infrastructure, legal structure, tracking behavior, or unrelated content was changed.

Before deployment, all four destinations returned HTTP 200 with valid TLS after redirects. Page titles were The Den of Tools - YouTube, 3D Print Rancher - YouTube, Never guess what a print costs again · Print Ranch Manager, and Jeff King - YouTube. Print Ranch Manager redirects from the approved URL to `https://manager.3dprintrancher.com/`; the site link deliberately retains the exact approved `https://www.printranchmanager.com`. No substitute or tracking URL was introduced. Reachability and page-title checks do not audit external services or guarantee their future availability.

Static checks passed for all four local pages, 37 internal link/asset/fragment references, landmarks, metadata, unique IDs, and absence of scripts/forms/embeds. Home-page responsive checks passed at 320, 375, 768 and 1440 pixels without horizontal overflow. All 14 home-page links were reached by keyboard with visible focus, including all four brand links. Brand targets measure at least 27 pixels high at tested widths. Existing text contrast remains above 4.5:1. These are basic accessibility checks, not a comprehensive WCAG audit.

After deployment, all four production HTTPS pages and CSS returned 200 and matched the local committed source byte for byte through normal DNS with valid TLS. All 15 alternate HTTP/apex/www combinations redirected to the corresponding HTTPS apex paths. This production content comparison confirms that the new links and CSS are deployed. No Pages source/domain, certificate, HTTPS, DNS, registrar, or email settings were changed.

No approved image files were found in the workspace/repository. Text identity remains in place. Approved horizontal lockup and RB monogram import is the only remaining non-blocking branding dependency.

## RBLP-004 — Approved logo integration

Ownership began at H-0012 (Protocol 1.0, CODEX, IN_PROGRESS), committed as `cf17c82`, following H-0011 and Jeff's explicit branding-only assignment.

All four supplied PNG originals are preserved byte for byte in `assets/brand/originals/`. Image 3 (`08_25_27 PM (3).png`) is unambiguously the horizontal lockup; Image 2 (`08_25_27 PM (2).png`) is the standalone color RB monogram. The two stacked variants are retained as originals only.

Asset preparation used deterministic Pillow crop/resize operations, without generative editing, tracing, redrawing, recoloring, filters, or aspect-ratio distortion:

- Horizontal original: 2172 × 724; alpha bounding box `(81, 160, 2114, 674)` cropped, then proportionally reduced to 1000 × 253 in `assets/brand/horizontal-lockup.png`. Every nontransparent source pixel is inside the crop.
- Monogram original: 1254 × 1254; alpha bounding box `(61, 130, 1192, 1228)` cropped and centered on a transparent 1257 × 1257 canvas, providing approximately 5% margin on each side. Derived PNGs are 32, 180, 192 and 512 pixels; root `favicon.ico` contains 16, 32 and 48 pixel frames.
- Original horizontal SHA-256: `9a8f1ca86adcb6cb784cd2e7452a7a593db06f4345ec98862448e28240a50760`.
- Original monogram SHA-256: `bb56091fe27d5ee6eeef93cd39f3ee18ba0d1920a1f8c486bbd1dda1c82d8663`.

Every page uses the horizontal image inside the existing home link, with `alt="Red Beard Studios LLC"` and the existing accessible home-link label. A 320-pixel maximum display width scales down proportionally on narrow screens. Native image-failure text was visually verified at 320 pixels by temporarily withholding the local image, then restoring it. No JavaScript fallback is needed. Icon declarations are present on all four pages, including the 180-pixel Apple touch icon. No app installation or service-worker functionality was added.

The shared primary colors now match the approved charcoal, deep red, warm ivory and warm gray tokens; existing readable muted text and subtle contact-panel background remain. The artwork itself retains its supplied colors. All four approved brand links and unrelated page content are unchanged. No DNS, registrar, Pages configuration, HTTPS, certificates, email records, analytics, tracking, legal structure, scripts or dependencies were changed or introduced.

Local verification passed: all four pages at 320, 375, 768 and 1440 pixels, no horizontal overflow, correctly loaded proportional header images; desktop/mobile visual inspection; all 14 home-page links reached by keyboard with 3-pixel visible focus; 57 local link/asset/fragment references; landmarks/metadata/unique IDs; no scripts/forms/embeds; all local pages/CSS return 200. Browser decoding passed for ICO and every PNG icon at its declared dimensions. Text contrast is at least 5.79:1 for tested foreground/background combinations. Production verification passed after successful Pages deployment `34672167591` of implementation commit `8e61703`: all four HTTPS pages, CSS, horizontal image, favicon ICO and all four PNG icons returned 200 with valid TLS and matched committed bytes exactly. All original supplied files were compared byte for byte, and all page anchors, main content and footers match the pre-integration version. Keyboard navigation also passed on privacy (11 links), terms (9) and accessibility (9). All four external brand destinations returned HTTPS 200 with valid TLS; Print Ranch Manager retains its approved URL and existing redirect to `https://manager.3dprintrancher.com/`.

Limitations: browser viewport testing is not a physical-device or comprehensive accessibility audit. OS home-screen installation and browser chrome icon selection/cache behavior are not exercised; icon files, declarations, dimensions and browser decoding are checked. Transparent approved artwork may have less contrast on dark browser chrome; artwork has not been recolored.

## RBLP-005 — CamoBot public listing

Jeff approved **CamoBot** as a fifth public Red Beard Studios LLC brand/project, with exact destination `https://camobot.com`. This task is post-launch content completion and does not authorize any infrastructure change.

Implementation commit `1629514` adds one normal same-tab anchor as the fifth item in the existing brand list, using exactly `https://camobot.com`. No CSS, artwork, icons, existing links, legal pages, infrastructure configuration or unrelated content changed.

Before deployment, all five approved destinations returned HTTPS 200 with valid TLS. CamoBot resolves to `https://camobot.com/` (same domain, trailing slash only), with title “CamoBot — Terrain-Matched Camouflage Pattern Generator”; no unexpected destination was observed. Print Ranch Manager retains its approved source URL and existing redirect to `https://manager.3dprintrancher.com/`.

Local verification passed at 320, 375, 768 and 1440 pixels with no horizontal overflow and all five exact approved URLs present. Desktop/mobile visual inspection passed. All 15 home-page links were reached by keyboard with visible 3-pixel focus outlines; brand targets are at least 27 pixels tall. Static checks passed for all four pages, 57 internal link/asset/fragment references, landmarks, metadata, unique IDs and absence of scripts/forms/embeds. The unchanged text palette retains a minimum tested contrast of 5.79:1. Browser viewport checks are not a physical-device or comprehensive accessibility audit; external reachability does not guarantee future availability.


Production deployment `34673160547` succeeded for `1629514`. All four public pages, CSS, header logo, favicon ICO and four PNG icon resources returned HTTPS 200 with valid TLS and matched committed files byte for byte, confirming CamoBot is deployed and existing branding is preserved.

## AI PROJECT HANDSHAKE

**Protocol Version:** 1.0

**Handshake:** H-0015

**Current Owner:** CHATGPT

**State:** LIVE — RBLP-005 COMPLETE

**Task ID:** RBLP-005

**Last Completed Action:**
Codex synchronized to H-0014 (`cae3de1`), read the handshake first and README in full, then added CamoBot as the fifth home-page brand using exactly `https://camobot.com`. The one-line implementation inherits existing brand styling and accessibility behavior. Existing logo, favicon, palette, four brand links, legal pages, layout and infrastructure are unchanged. Implementation `1629514` is pushed and deployed.

**Verification Results and Limitations:**
All five approved destinations returned HTTPS 200 with valid TLS before deployment. CamoBot stayed on `https://camobot.com/`, with the expected CamoBot terrain-matched camouflage generator title; no unexpected redirect was observed. Print Ranch Manager retains its approved URL and existing redirect to `https://manager.3dprintrancher.com/`. The exact five link attributes were verified at 320, 375, 768 and 1440 pixels with no horizontal overflow. Desktop/mobile visual checks passed. All 15 home-page links were keyboard reachable with visible 3-pixel focus; brand targets are at least 27 pixels tall. Static checks passed for all four pages and 57 internal references, semantic structure and no scripts/forms/embeds. No new dependencies or tracking were added.

Pages deployment `34673160547` succeeded. All four public HTTPS pages, CSS, header image and five icon resources returned 200 with valid TLS and matched committed bytes exactly. Browser viewport testing is not a physical-device or comprehensive accessibility audit. External reachability is a point-in-time check.

**Next Required Action:**
CHATGPT: review the live fifth-brand listing and RBLP-005 verification record. Preserve the live configuration. Define a new scoped task and numbered handshake if further work is required.

**Blockers:**
None, including no remaining content or asset dependency for RBLP-005.

**Commit / Push Status:**
Implementation commit `1629514` is pushed to `origin/main` and deployed. This documentation-only H-0015 handoff is committed and pushed in the following commit; its exact hash is reported in the final response to avoid a self-referential hash.

**Working-tree Status:**
Clean after the handoff commit, with local `main` synchronized to `origin/main`; final status and matching commit IDs are verified after push.

## Handshake Rules

README.md is the single source of truth for project state.

Whenever ChatGPT or Codex begins or resumes work:

1. Read the latest committed README.md.
2. Read the AI PROJECT HANDSHAKE section first.
3. Identify Protocol Version, Handshake, Current Owner, State, Task ID, Last Completed Action, Next Required Action, and Blockers.
4. Compare the repository handshake with any previously known state.
5. Discard stale remembered state whenever the repository is newer.
6. Do not perform implementation work unless the handshake assigns ownership appropriately.
7. The party completing its assigned task must update the handshake before handing ownership to the next party.

Every handoff must be complete in both README.md and the final user-facing response. Include Protocol Version, Handshake number, Current Owner, State, Task ID, Last Completed Action, verification results and limitations, exact next required action, blockers (including non-blocking dependencies), commit/push status, and working-tree status. Do not substitute a short status summary for the full handoff. This is Jeff's persistent handoff preference.

Conversation history and memory are subordinate to the current committed README.md.