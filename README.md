# Red Beard Studios LLC Corporate Landing Page

Corporate website for **Red Beard Studios LLC**, a Montana-based company operating media, software, ecommerce, and digital product businesses.

Canonical public domain: **https://Red-Beard.com**

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

## Approved V1 Public Brands / Projects

- The Den of Tools
- 3D Print Rancher
- Print Ranch Manager

Do not add experimental, private, unreleased, or other Red Beard Studios LLC projects unless Jeff explicitly approves them for public listing.

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

- Red Beard Studios LLC corporate identity
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

### Identity / Logo

Jeff confirmed the official public identity is **Red Beard Studios LLC**. This supersedes the earlier working identity **Red Beard LLC** for public-facing site branding.

Jeff has supplied approved production logo artwork outside the repository, including a primary stacked logo, standalone RB monogram, horizontal lockup, and one-color black version. The preferred website treatment is the horizontal lockup in the site header and the RB monogram for favicon/app-icon use when those files are available in the implementation workspace or repository.

Until the production logo assets are available to Codex in the repository/workspace, a restrained text-based identity remains acceptable and is not a launch blocker. Do not invent or redraw logo assets.

Brand direction remains premium, understated, and modern. Approved palette from the supplied brand sheets:

- Charcoal Black: `#111111`
- Deep Red: `#8E1F1F`
- Warm Ivory: `#F5F2ED`
- Warm Gray: `#B8B0A6`

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

### Production launch status — LIVE

As of **2026-09-12 03:15 UTC**, production is **LIVE** at **https://red-beard.com** under the approved public identity **Red Beard Studios LLC**. HTTPS is enforced, certificates validate for apex and www, and all required pages and CSS pass through normal public DNS. The approved logo files are not present in the repository/workspace, so the corrected temporary text identity remains in use.

#### H-0008 final launch and identity verification

- Updated all four HTML pages: public company references, header identity and accessible labels, titles, descriptions, Open Graph metadata, legal/privacy/accessibility copy, mailing-address company names, and copyright now say Red Beard Studios LLC. Domain, email, postal address, page structure, and approved brands are preserved. Implementation commit: `e23fb2c`.
- No logo assets were found in the workspace/repository. No logo or monogram was redrawn. Horizontal lockup and favicon/app-icon integration remain dependent on importing Jeff's approved files. The existing accessible temporary styling remains; the documented production palette is available for the eventual logo integration.
- Public DNS returns all four GitHub A addresses and www CNAME redbeardrex.github.io. Normal HTTP clients now reach GitHub; the previously observed stale local DNS destination is no longer blocking verification. No GoDaddy settings were changed in this pass.
- Restarted stalled certificate provisioning by removing and immediately restoring the GitHub Pages custom-domain setting, following [GitHub's documented procedure](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https). GitHub automatically committed CNAME removal/restoration (`2baa443`, `d13e9aa`) and normalized its value to lowercase `red-beard.com`; the domain is unchanged. Both remote commits were fast-forwarded into the workspace before the identity commit.
- GitHub's certificate is approved for red-beard.com and www.red-beard.com, expiring December 10, 2026. Enabled HTTPS enforcement and verified the API reports `https_enforced: true`.
- [Deployment 34669826392](https://github.com/RedBeardRex/RedBeardLLC/actions/runs/34669826392) built commit `e23fb2c` successfully. The final Pages build status is built with no error.
- All five HTTPS apex paths (`/`, `/privacy.html`, `/terms.html`, `/accessibility.html`, `/css/styles.css`) return HTTP 200 and match local committed files byte for byte using normal DNS, without IP overrides or bypassing certificate validation.
- All 20 combinations of HTTP/HTTPS, apex/www, and the five paths finish at the corresponding HTTPS apex path with HTTP 200 and valid TLS. During the first check, HTTP www root used an intermediate HTTP apex redirect; the full chain still reached the HTTPS apex correctly. All paths were preserved.
- Re-ran static validation: 37 internal links/assets/fragments, unique IDs, landmarks, language, viewport and canonical metadata passed. All four pages were checked at 320, 375, 768 and 1440 pixels without horizontal overflow. Keyboard skip link retained visible focus and moved focus to main. Existing text contrast remains 5.79:1–13.98:1; no scripts, trackers or dependencies were added. These are basic accessibility checks, not a full WCAG or assistive-technology audit.

#### H-0006 DNS changes and verification

- Used the authenticated GoDaddy session for `red-beard.com`. Removed the YouTube forwarding rule after Jeff's explicit confirmation at the deletion prompt. GoDaddy now shows both domain and subdomain forwarding as **Not set up**.
- Removing forwarding restored GoDaddy's default apex parking record and a `www` alias. Changed that apex record to `185.199.108.153`, added `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`, and updated the restored `www` CNAME to `redbeardrex.github.io`. All five records use TTL 3600 (1 Hour). GoDaddy confirmed successful saves.
- Both authoritative nameservers, `ns19.domaincontrol.com` and `ns20.domaincontrol.com`, return exactly the four GitHub apex A addresses and the `www` CNAME above. No old forwarding/parking A values remain and there are no apex AAAA records.
- Cloudflare (`1.1.1.1`) and Google (`8.8.8.8`) DNS also return the four GitHub A values and correct `www` CNAME. Nameservers remain unchanged.
- Reviewed all three pages of the resulting DNS table. Existing Google mail MX records, SPF/DKIM/DMARC TXT records, email CNAMEs, the `pay` subdomain, and default NS/SOA records remain present. No edits were made to those records or to any account, billing, ownership, privacy, renewal, or security settings. No wildcard records were added.
- Re-saved the existing GitHub Pages custom domain `red-beard.com` after correcting DNS. Pages remains built from `main` at `/`; the committed `CNAME` remains `Red-Beard.com`.
- At the GitHub IP returned by public DNS, all five HTTP paths (`/`, `/privacy.html`, `/terms.html`, `/accessibility.html`, `/css/styles.css`) return 200 and match the repository files byte for byte. HTTP `www` requests for all five paths return 301 to the matching apex HTTP path.
- Those endpoint checks used `curl --resolve` with `185.199.108.153` because this machine's default HTTP client still connected to the cached old address `3.33.251.168` and returned 404, even after DNS queries returned the new addresses. These results establish destination readiness, not expiration of every resolver/client cache.
- HTTPS at the GitHub destination failed hostname certificate validation for both apex and `www` at H-0007. No TLS validation was bypassed. At that time the Pages API reported `https_certificate: null` and `https_enforced: false`.

The launch work pending at H-0007 was completed during H-0008 as recorded above. This subsection is historical.

#### Earlier H-0004 launch record (historical)

The following deployment actions and response results describe the initial launch attempt before the H-0006 DNS changes above.

#### Completed launch actions

- Fast-forwarded the workspace to authoritative main at `23d686d`; read H-0004 first and README.md in full.
- Verified that the repository is public and the available GitHub credentials have administration permission. Pages was not enabled (`has_pages: false`).
- Enabled GitHub Pages with branch publishing (`build_type: legacy`), source `main`, directory `/`. GitHub retained the custom domain `red-beard.com`; the committed `CNAME` remains exactly `Red-Beard.com`.
- [Pages deployment 34661756167](https://github.com/RedBeardRex/RedBeardLLC/actions/runs/34661756167) completed successfully for `23d686d`. The Pages API reports `status: built` with no build error.
- Requested HTTPS enforcement. GitHub returned HTTP 404, “The certificate does not exist yet.” Its API reports `https_certificate: null` and `https_enforced: false`. Enforcement must be retried after DNS points to GitHub and the certificate is issued.
- No registrar settings, DNS records, site content, analytics, or dependencies were changed.

#### Initial verification results (before DNS changes)

| Check | Result |
| --- | --- |
| GitHub origin: `/`, `/privacy.html`, `/terms.html`, `/accessibility.html`, `/css/styles.css` | All HTTP 200; response bytes exactly match the committed source. Tested using `curl --resolve red-beard.com:80:185.199.108.153` to reach GitHub directly. This is an origin check, not public DNS or custom-domain HTTPS success. |
| Public `http://red-beard.com/` and `https://red-beard.com/` | Both HTTP 301 to `http://www.youtube.com/@denoftools`; old forwarding is still active. |
| Public HTTPS legal pages and stylesheet | All HTTP 404 from the current non-GitHub destination. |
| `http://www.red-beard.com/` and `https://www.red-beard.com/` | DNS resolution failed. |
| `https://redbeardrex.github.io/RedBeardLLC/` | HTTP 301 to `http://red-beard.com/`; GitHub's default URL honors the configured custom domain. |
| TLS | Current apex forwarding endpoint and default GitHub hostname pass certificate verification. This does not verify a GitHub certificate for the custom domain. GitHub custom-domain TLS is pending. No certificate validation was bypassed. |
| Canonical metadata | Deployed HTML matches source, including HTTPS apex canonical URLs. Public host redirects do not yet implement the desired canonical behavior. |

#### Exact GoDaddy changes — explicitly authorized by Jeff

Jeff authorized and Codex completed the following production DNS and forwarding changes in GoDaddy for `red-beard.com`. These steps are historical and **must not be repeated** unless a new problem is discovered and ChatGPT/Jeff explicitly authorizes a correction.

| Type | Name / Host | Value / Points to | TTL |
| --- | --- | --- | --- |
| A | @ | 185.199.108.153 | 1 hour |
| A | @ | 185.199.109.153 | 1 hour |
| A | @ | 185.199.110.153 | 1 hour |
| A | @ | 185.199.111.153 | 1 hour |
| CNAME | www | redbeardrex.github.io | 1 hour |

Existing nameservers, MX, TXT, email, verification, unrelated subdomain, billing, ownership, privacy, renewal, and security settings were left unchanged.

## AI PROJECT HANDSHAKE

**Protocol Version:** 1.0

**Handshake:** H-0009

**Current Owner:** CHATGPT

**State:** LIVE

**Task ID:** RBLP-002

**Last Completed Action:**
Codex synchronized with H-0008, read the handshake first and README.md in full, updated every public company-name reference and metadata field to Red Beard Studios LLC, and published implementation commit e23fb2c. Restarted stalled GitHub certificate provisioning, enabled HTTPS enforcement after issuance, and verified the successful deployment. All five HTTPS apex resources match the committed source; all 20 host/scheme/path combinations reach the correct HTTPS apex URL with valid TLS. Static/link, responsive and keyboard accessibility checks passed. No GoDaddy changes were repeated. Logo assets were absent, so the corrected temporary text identity remains. Full handoff requirements were added to the protocol at Jeff's request.

**Verification:**
Production is LIVE as of 2026-09-12 03:15 UTC. Pages builds from main at /, certificate covers apex and www, and HTTPS enforcement is enabled. HTTP 200, source equality, normal DNS, valid TLS, complete redirect chains, path preservation, 37 local links and four responsive widths passed. See the H-0008 verification record above for exact scope and limitations.

**Branding Status:**
Text and metadata identity correction is complete and deployed. Approved horizontal lockup and RB monogram integration are pending asset import; no replacement artwork was invented.

**Next Required Action:**
ChatGPT must synchronize with main, read H-0009 first and README.md in full, review the live Red Beard Studios LLC site, and report launch completion to Jeff. Obtain/import the approved horizontal lockup and RB monogram files into the repository/workspace, then issue a separately scoped branding task through the next numbered handshake for header and favicon/app-icon integration using the approved palette. Approved brand destination URLs can be handled in a later scoped task. Do not repeat completed GoDaddy or HTTPS configuration.

**Blockers:**
No launch blockers remain. Approved logo files are not available in the repository/workspace; this blocks only logo/favicon integration. Approved brand destination URLs remain a non-blocking future input.

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