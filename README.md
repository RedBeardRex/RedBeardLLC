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

### Production launch status — BLOCKED_ON_DNS

Launch task RBLP-002 was executed on September 11, 2026 (America/Denver), following Jeff's approval in H-0004. GitHub deployment succeeded; the canonical public domain is still using the old forwarding service. Production is **BLOCKED_ON_DNS**, not live at the intended domain.

#### Completed launch actions

- Fast-forwarded the workspace to authoritative main at `23d686d`; read H-0004 first and README.md in full.
- Verified that the repository is public and the available GitHub credentials have administration permission. Pages was not enabled (`has_pages: false`).
- Enabled GitHub Pages with branch publishing (`build_type: legacy`), source `main`, directory `/`. GitHub retained the custom domain `red-beard.com`; the committed `CNAME` remains exactly `Red-Beard.com`.
- [Pages deployment 34661756167](https://github.com/RedBeardRex/RedBeardLLC/actions/runs/34661756167) completed successfully for `23d686d`. The Pages API reports `status: built` with no build error.
- Requested HTTPS enforcement. GitHub returned HTTP 404, “The certificate does not exist yet.” Its API reports `https_certificate: null` and `https_enforced: false`. Enforcement must be retried after DNS points to GitHub and the certificate is issued.
- No registrar settings, DNS records, site content, analytics, or dependencies were changed.

#### Verification results

| Check | Result |
| --- | --- |
| GitHub origin: `/`, `/privacy.html`, `/terms.html`, `/accessibility.html`, `/css/styles.css` | All HTTP 200; response bytes exactly match the committed source. Tested using `curl --resolve red-beard.com:80:185.199.108.153` to reach GitHub directly. This is an origin check, not public DNS or custom-domain HTTPS success. |
| Public `http://red-beard.com/` and `https://red-beard.com/` | Both HTTP 301 to `http://www.youtube.com/@denoftools`; old forwarding is still active. |
| Public HTTPS legal pages and stylesheet | All HTTP 404 from the current non-GitHub destination. |
| `http://www.red-beard.com/` and `https://www.red-beard.com/` | DNS resolution failed. |
| `https://redbeardrex.github.io/RedBeardLLC/` | HTTP 301 to `http://red-beard.com/`; GitHub's default URL honors the configured custom domain. |
| TLS | Current apex forwarding endpoint and default GitHub hostname pass certificate verification. This does not verify a GitHub certificate for the custom domain. GitHub custom-domain TLS is pending. No certificate validation was bypassed. |
| Canonical metadata | Deployed HTML matches source, including HTTPS apex canonical URLs. Public host redirects do not yet implement the desired canonical behavior. |

#### Exact manual GoDaddy changes

Public registry RDAP identifies the registrar as **GoDaddy.com, LLC**. The authoritative nameservers are `ns19.domaincontrol.com` and `ns20.domaincontrol.com`. Authoritative DNS currently returns apex A records `15.197.225.128` and `3.33.251.168` with TTL 3600; there are no apex AAAA records and no `www` A, AAAA, or CNAME answers. No connected registrar tool or open registrar session was available, so the following changes remain for Jeff.

1. Sign in to GoDaddy, open **Domain Portfolio**, select **red-beard.com**, and open **DNS**.
2. Under **Forwarding**, remove the domain forwarding to `http://www.youtube.com/@denoftools` (and any `www` forwarding if present). The current public redirect was verified; the account's exact forwarding settings were not accessible. If forwarding locks the current A records, remove forwarding first, then reopen DNS records.
3. Replace the two old apex A values, `15.197.225.128` and `3.33.251.168`, with the four GitHub Pages A records below. Add the `www` CNAME. Ensure the final set has all four A values, no old forwarding A values, and only one CNAME for `www`.

| Type | Name / Host | Value / Points to | TTL |
| --- | --- | --- | --- |
| A | @ | 185.199.108.153 | 1 hour |
| A | @ | 185.199.109.153 | 1 hour |
| A | @ | 185.199.110.153 | 1 hour |
| A | @ | 185.199.111.153 | 1 hour |
| CNAME | www | redbeardrex.github.io | 1 hour |

4. Save the records. The CNAME target is only `redbeardrex.github.io`, with no `https://` prefix and no `/RedBeardLLC` path. Leave the existing nameservers and unrelated MX, TXT, email, and subdomain records unchanged. No apex AAAA records are required for this IPv4 configuration; do not add conflicting apex addresses or a wildcard record.
5. Confirm the new A records and `www` CNAME have propagated. GoDaddy advises that changes commonly take effect within an hour but may take up to 48 hours globally.
6. Open [repository Pages settings](https://github.com/RedBeardRex/RedBeardLLC/settings/pages). Keep **Deploy from a branch → main → / (root)** and custom domain **red-beard.com**. Once the DNS check succeeds and GitHub issues the certificate, enable **Enforce HTTPS**. GitHub advises HTTPS availability may take up to an hour after correct custom-domain configuration.
7. Return the task for verification: all four pages and CSS must load over `https://red-beard.com`; HTTP must redirect to HTTPS; both `www` schemes must reach the HTTPS apex, preserving paths; certificates must validate for apex and `www`. Then record LIVE in a new handshake.

DNS values and expected apex/`www` redirects were checked against [GitHub custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) and [GitHub HTTPS guidance](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https). GoDaddy's [A record instructions](https://www.godaddy.com/en-uk/help/add-or-edit-an-a-record-42546) and [CNAME instructions](https://www.godaddy.com/en-uk/help/edit-a-cname-record-19237) explain the DNS editor. Account-level Pages domain verification, if requested by GitHub, requires its generated TXT value; no verification token has been invented.

## AI PROJECT HANDSHAKE

**Protocol Version:** 1.0

**Handshake:** H-0005

**Current Owner:** CHATGPT

**State:** BLOCKED_ON_DNS

**Task ID:** RBLP-002

**Last Completed Action:**
Codex synchronized to H-0004 and executed the authorized launch task. GitHub Pages was enabled from main at the repository root, preserving CNAME for Red-Beard.com. Deployment 34661756167 succeeded; all four pages and CSS were verified at the GitHub origin with HTTP 200 and exact source matches. Public apex DNS still points to the old YouTube forwarding service, and www has no DNS answer. GitHub's custom-domain certificate is not yet issued, so HTTPS enforcement could not be enabled. Exact GoDaddy records, manual steps, public response results, and remaining checks are recorded above. Production status is BLOCKED_ON_DNS.

**Next Required Action:**
ChatGPT must read H-0005 first and README.md in full, guide Jeff through the documented GoDaddy forwarding removal and DNS changes, then issue the next numbered handshake assigning CODEX to verify DNS propagation, GitHub certificate issuance, HTTPS enforcement, apex/www redirects, all four public pages, and CSS. Record LIVE only after those checks pass. Jeff's production-launch approval remains in effect; no new product approval is needed for these already authorized launch steps.

**Blockers:**
Manual GoDaddy forwarding/DNS changes are required because registrar access was unavailable. GitHub custom-domain certificate issuance and HTTPS enforcement await correct DNS. No product, code, or GitHub configuration-permission blockers remain. Official logo and approved brand destination URLs remain non-blocking post-launch items.

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
