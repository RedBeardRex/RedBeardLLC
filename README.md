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

Jeff has supplied approved production logo artwork outside the repository, including:

- primary stacked logo
- standalone RB monogram
- horizontal lockup
- one-color black version

Preferred web treatment when the approved files are available in the implementation workspace/repository:

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
- Approved logo artwork: supplied to ChatGPT in the project conversation, but not yet confirmed present in the Codex workspace/repository.
- Temporary text identity: currently acceptable until approved files are imported.
- Approved brand destinations: now supplied and locked above.
- Approved public brand list now contains four entries, including **Coach Jeff King**.

## AI PROJECT HANDSHAKE

**Protocol Version:** 1.0

**Handshake:** H-0010

**Current Owner:** CODEX

**State:** READY_FOR_BRAND_POLISH

**Task ID:** RBLP-003

**Last Completed Action:**  
ChatGPT reviewed H-0009 after successful production launch. Jeff supplied the approved public destination URLs for The Den of Tools, 3D Print Rancher, Print Ranch Manager, and a newly approved fourth public channel, Coach Jeff King. ChatGPT validated the canonical The Den of Tools YouTube handle as `https://www.youtube.com/@denoftools` and recorded all four destinations in this README. The site remains LIVE and no infrastructure change is required.

**Verification:**  
RBLP-002 launch verification remains valid: production is live at `https://red-beard.com`, HTTPS is enforced, apex/www behavior and required resources passed. No DNS, GoDaddy, certificate or hosting changes are required for RBLP-003. The four destination URLs are authoritative product inputs for the next implementation pass; Codex must verify each reachable destination as part of implementation.

**Branding Status:**  
Public text identity is Red Beard Studios LLC. Approved horizontal lockup and RB monogram exist outside the repository but may still need to be imported into the Codex workspace/repository. Approved brand links are now available. The approved public brand list is The Den of Tools, 3D Print Rancher, Print Ranch Manager, and Coach Jeff King.

**Next Required Action:**  
Codex must synchronize to `main`, read H-0010 first and README.md in full, then perform RBLP-003 as a narrowly scoped branding/polish pass:

1. Update the home-page brands section so all four approved brands/projects are present and clickable using exactly these destinations:
   - The Den of Tools → `https://www.youtube.com/@denoftools`
   - 3D Print Rancher → `https://www.youtube.com/@3dprintrancher`
   - Print Ranch Manager → `https://www.printranchmanager.com`
   - Coach Jeff King → `https://www.youtube.com/@CoachJeffKing`
2. Preserve semantic HTML, keyboard accessibility, visible focus, responsive behavior, and the current restrained premium design.
3. Verify all four external destinations before deployment. If one is unreachable or clearly wrong, do not invent a substitute; report the exact issue in the handoff.
4. If Jeff's approved production logo files are available in the workspace/repository, import them into sensible `assets/` paths, use the horizontal lockup in the header and the RB monogram for favicon/app-icon use, preserving accessible text/fallback behavior. Do not redraw or approximate the artwork.
5. If the logo files are not available to Codex, leave the current text identity in place and mark logo integration as the only remaining non-blocking dependency.
6. Do not change GoDaddy, DNS, nameservers, MX/TXT records, GitHub Pages source/domain settings, certificates, HTTPS enforcement, analytics/tracking behavior, or unrelated site scope.
7. Run link/static checks, responsive checks at the existing widths, keyboard/focus checks, and a public production smoke test after deployment.
8. Commit and push all approved changes to `main`.
9. Update README to H-0011 with Current Owner CHATGPT and report exact implementation, verification, commit/push status, working-tree status, and any remaining blocker/dependency.

**Blockers:**  
No blocker for adding the four brand links. Logo/header/favicon integration is blocked only if the approved image files are not available in the Codex workspace/repository. This asset dependency is non-blocking for the link update and must not delay deployment of the approved brand links.

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