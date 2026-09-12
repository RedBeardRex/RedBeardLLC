# Red Beard LLC Corporate Landing Page

Corporate website for **Red Beard LLC**, a Montana-based company operating media, software, ecommerce, and digital product businesses.

Canonical public domain: **https://Red-Beard.com**

Public contact email: **info@red-beard.com**

Public mailing address:

1106 W. Park Street Suite 20 # 142  
Livingston, MT 59047

## Project Purpose

This site is intentionally small. It serves as:

- the public corporate home for Red Beard LLC;
- proof of legitimacy for customers, partners, payment providers, OAuth providers, and other services;
- the canonical parent-company identity for approved Red Beard LLC products and brands;
- a stable location for company contact and legal information.

It is not intended to be a large marketing site or creator landing page.

## Approved V1 Public Brands / Projects

- The Den of Tools
- 3D Print Rancher
- Print Ranch Manager

Do not add experimental, private, unreleased, or other Red Beard LLC projects unless Jeff explicitly approves them for public listing.

## Hosting and Infrastructure

Preferred hosting: **GitHub Pages**

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
- DNS may remain managed by the current registrar and point to GitHub Pages

## V1 Site Architecture

Keep the implementation intentionally small:

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

A separate Brands page is not required for V1. Approved brands can be presented cleanly on the home page.

### Home Page

Include:

- Red Beard LLC corporate identity
- concise positioning statement: a Montana-based media, software, ecommerce, and digital products company
- brief About section
- approved public brands/projects
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

Add an affiliate disclosure only if the Red Beard LLC corporate site itself contains affiliate links.

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

### Identity / Logo

An official Red Beard LLC logo is being completed and will be supplied later.

The logo is **not a blocker** for initial implementation. Until the approved logo is available, use a restrained text-based **Red Beard LLC** identity that can be replaced cleanly without redesigning the site.

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

## V1 Implementation and Verification

Implemented on September 11, 2026 under RBLP-001; site implementation commit: `7c8f921`.

- Four static pages: home, privacy, terms, and accessibility; shared responsive CSS and `CNAME` containing `Red-Beard.com`.
- Restrained text identity, all three approved public brands, approved email and mailing address, consistent navigation and copyright.
- Semantic HTML, skip link, visible keyboard focus, descriptive page titles, descriptions, canonical URLs, and Open Graph metadata.
- No JavaScript, framework, analytics, trackers, cookies, forms, remote fonts, or other third-party asset dependencies. Brand names are listed without links because approved destination URLs were not supplied.
- Privacy copy describes the site's behavior and GitHub Pages security logging, with links to GitHub documentation. Legal and accessibility copy is prepared for review; accessibility wording does not claim certified conformance.

### Local preview and maintenance

No install or build step is needed. From the repository root, run `python3 -m http.server 8765 --bind 127.0.0.1` and open `http://127.0.0.1:8765/`. Stop the server with Ctrl+C. Edit the HTML pages and `css/styles.css` directly; navigation and footer markup are shared by convention and should be kept consistent across all four pages.

### Verification performed

- Local HTTP checks: all four pages and the shared stylesheet returned HTTP 200.
- Static checks: 37 local link, asset, and fragment references resolved; unique IDs, one main landmark and H1 per page, language and viewport declarations, canonical metadata, and absence of scripts, forms, and embeds verified.
- Browser checks: all four pages rendered at 320, 375, 768, and 1440 CSS-pixel viewport widths without horizontal overflow. Desktop and mobile screenshots were inspected alongside rendered DOM geometry.
- Keyboard checks: all 10 home-page links reached in logical order with visible focus; activating the skip link moved focus to main. Privacy, Terms, Accessibility, and the cross-page Brands anchor navigation worked.
- Text contrast: all six text/background color combinations exceeded 4.5:1 (measured range 5.79:1–13.98:1).
- `git diff --check` passed. These are basic accessibility and static-site checks, not a complete WCAG audit; screen-reader testing, browser text enlargement, and additional browser engines remain review opportunities.

### Production launch status

Production launch requires Jeff's approval under this charter. No Pages settings, DNS records, or HTTPS settings were changed. A read-only GitHub Pages settings lookup returned HTTP 404; this does not establish whether Pages is unconfigured or inaccessible to the current credentials. Production domain behavior and HTTPS have not been verified.

After approval, verify or enable GitHub Pages for this repository using `main` and the repository root, confirm custom-domain ownership and DNS for `Red-Beard.com`, and verify HTTPS and every public page. Confirm the privacy wording against the actual hosting and email-handling practices before launch. The pending official logo remains non-blocking for implementation.

## AI PROJECT HANDSHAKE

**Protocol Version:** 1.0

**Handshake:** H-0003

**Current Owner:** CHATGPT

**State:** READY_FOR_REVIEW

**Task ID:** RBLP-001

**Last Completed Action:**  
Codex synchronized the existing workspace with the authoritative remote main, read H-0002 first and README.md in full, and implemented the complete V1 static corporate website in commit `7c8f921`, which was pushed to main. The implementation includes index.html, privacy.html, terms.html, accessibility.html, css/styles.css, and CNAME for Red-Beard.com. The approved text identity, three public brands, contact information, legal pages, responsive layout, keyboard support, and basic metadata are present. Local link, HTTP, responsive, keyboard, and contrast checks passed as detailed above. No implementation blockers remain. This H-0003 handoff returns ownership to ChatGPT for review.

**Next Required Action:**  
ChatGPT must synchronize with main, read H-0003 first and README.md in full, review the V1 implementation and verification against the charter, and present it to Jeff for public identity, content, legal/privacy wording, and production-launch approval. Confirm that the privacy wording matches actual hosting and email practices. Obtain approved brand destination URLs if links are desired and the official logo when available. After review, either record approval and assign a clearly scoped launch task or issue a specific revision task to CODEX through the next numbered handshake. Do not launch or change hosting/DNS settings before Jeff approves production launch.

**Blockers:**  
None for the completed V1 implementation. Production launch awaits Jeff's approval and verification/configuration of GitHub Pages, DNS, and HTTPS. The Pages settings lookup returned HTTP 404, so hosting configuration remains unconfirmed. Official logo and approved brand destination URLs are pending, non-blocking items for review.

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

Conversation history and memory are subordinate to the current committed README.md.
