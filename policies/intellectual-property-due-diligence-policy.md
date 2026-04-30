# CoinPort Intellectual Property Due Diligence Policy and Procedures

| Field | Value |
| --- | --- |
| Document owner | CoinPort Engineering |
| Classification | Internal |
| Version | 1.0 |
| Effective date | 2026-02-30 |
| Next review | 2027-02-30 |
| Approver | CoinPort CTO |

---

## 1. Purpose

This policy establishes the due-diligence framework that CoinPort Pty Ltd (ABN 12 624 879 223, "**CoinPort**") follows to ensure that the CoinPort cryptocurrency exchange (`www.coinport.com.au`) and the corporate operations supporting it do not infringe the intellectual property (IP) rights of any third party.

CoinPort Exchange is built on the **OpenDAX** open-source stack and incorporates a substantial number of additional open-source libraries, container images, fonts, icons, images, third-party SaaS components, and contributed code. Each of these brings a license, trademark posture, and authorship history that CoinPort must respect. The objective of this policy is to ensure that:

- Every component CoinPort distributes, runs, or relies on is used within the terms of its licence.
- CoinPort's own trademarks, branding, and copyrighted material are clearly distinguishable from those of upstream projects.
- CoinPort does not knowingly incorporate code, designs, or content that is encumbered by a third party's copyright, patent, trademark, or trade-secret rights without authorisation.
- A defensible, auditable record exists of how each component entered the platform and on what terms.

## 2. Scope

This policy applies to:

- All software included in or operated by the CoinPort Exchange, including the OpenDAX-derived service stack (Peatio, Barong, AppLogic, Sonic, Tower, Gateway/Envoy, Rango, Traefik, Vault, Redis, RabbitMQ, MySQL, PostgreSQL, and all Peatio daemons), the orchestration layer in the `opendax` repository, container images pulled from public registries, and forks maintained under the `github.com/coinport` organisation.
- All third-party SaaS components integrated with the platform, including but not limited to SendGrid, Twilio, Didit, KYCAID, Cloudflare, Auth0, Firebase, MaxMind, IPInfo, Monoova, TradingView, Telegram, Microsoft Teams, Freshworks, Google Analytics / Tag Manager / Clarity.
- All non-code assets used by CoinPort: trademarks, logos, brand names, icons, fonts, images, illustrations, copy, marketing material, training material, and documentation.
- All contributions to CoinPort code or content from employees, contractors, agencies, interns, and external contributors.
- All internally generated IP (custom code, designs, KYC workflows, internal tools, blockchain integrations) that CoinPort owns or claims rights in.

This policy applies to every CoinPort director, officer, employee, contractor, and agent who designs, builds, deploys, markets, or supports the CoinPort Exchange.

## 3. Definitions

| Term | Meaning |
| --- | --- |
| IP | Intellectual property: copyright, patents, trademarks, designs, trade secrets, database rights, and moral rights. |
| Open-source software (OSS) | Software made available under a licence approved by the Open Source Initiative or a licence with substantively similar terms (e.g. Apache-2.0, MIT, BSD, MPL, LGPL, GPL, AGPL). |
| Permissive licence | An OSS licence that allows use, modification, and redistribution with minimal obligations beyond attribution and notice (e.g. MIT, BSD-2/3-Clause, Apache-2.0, ISC). |
| Copyleft licence | An OSS licence that requires derivative works to be distributed under the same or compatible terms (e.g. GPL-2.0, GPL-3.0, LGPL, AGPL, MPL-2.0). |
| Strong copyleft | Copyleft that extends to network-deployed services (e.g. AGPL-3.0). |
| SBOM | Software Bill of Materials: a structured inventory of every component (and its licence) used by the platform. |
| Notice file | A file (typically `NOTICE`, `THIRD_PARTY_NOTICES.md`, or `licenses/`) listing third-party components, their copyright notices, and their licences. |
| Component | Any external item brought into CoinPort: a library, container image, font, icon set, image, dataset, API, snippet, design, document, or piece of marketing copy. |
| Contributor | Any person who creates code or content for CoinPort, whether as employee, contractor, agency, intern, or external collaborator. |
| Upstream | The original project from which CoinPort takes a component (e.g. OpenWare for OpenDAX, Peatio, Barong; Hashicorp for Vault). |

## 4. Roles and Responsibilities

| Role | Responsibility |
| --- | --- |
| **CTO** | Owner of this policy. Approves licence-tier exceptions, signs off on the annual IP review, and represents CoinPort in any infringement notice or dispute. |
| **Engineering Lead** | Operates the day-to-day procedures: SBOM generation, dependency review, fork hygiene, and technical sign-off on new components. |
| **Engineers and Contractors** | Comply with the procedures in Sections 6–10 before introducing any new component, asset, or contribution. Raise IP concerns via the escalation path in Section 12. |
| **Marketing / Brand** | Operates the procedures in Section 9 (trademarks and brand assets), including font, icon, image, and copy clearance. |
| **Legal Counsel** | Engaged for external IP advice, licence interpretation in ambiguous cases, contractor IP-assignment drafting, and any infringement notice received or sent. CoinPort uses external counsel; the CTO is the internal escalation point. |
| **All staff** | Report any actual or suspected IP issue to the CTO immediately. |

## 5. IP Risk Inventory

CoinPort's IP risk surface is composed of the following categories. Each is governed by the corresponding procedure in Sections 6–10.

| # | Category | Examples specific to CoinPort | Governing procedure |
| --- | --- | --- | --- |
| 1 | OpenDAX-derived services | Peatio, Barong, AppLogic, Sonic, Tower, Rango, Gateway | §6, §7 |
| 2 | Forked repositories under `github.com/coinport` | Forks of upstream OpenWare, Peatio, Barong, etc. | §7 |
| 3 | Open-source libraries (Ruby gems, npm packages, Go modules, Python packages) | Gems listed in `Gemfile`/`Gemfile.lock`, frontend packages, daemon dependencies | §6 |
| 4 | Container images and base images | `redis`, `rabbitmq`, `vault`, `traefik`, MySQL/PostgreSQL clients, custom CoinPort images | §6 |
| 5 | Third-party SaaS / APIs | SendGrid, Twilio, Didit, KYCAID, Cloudflare, Auth0, Firebase, MaxMind, IPInfo, Monoova, TradingView, Google Analytics / Tag Manager / Clarity | §8 |
| 6 | Trademarks and brand assets | "CoinPort" name and logo, OpenDAX/Peatio/Barong upstream marks, third-party logos used in UI | §9 |
| 7 | Fonts, icons, images, illustrations | Frontend fonts, marketing imagery, icon sets, KYC document samples, blog imagery | §9 |
| 8 | Marketing and educational copy | Website copy, blog posts, help articles, social posts, training material | §9 |
| 9 | Custom CoinPort code and configuration | Code in `lib/opendax/`, ERB templates, Rake tasks, CoinPort-only frontend changes | §10 |
| 10 | Contributed code and content | Work product of contractors, agencies, interns, and external contributors | §10 |
| 11 | Patents | Crypto-exchange-related claims potentially held by third parties (US and AU); CoinPort holds none at present | §11 |

## 6. Due Diligence — Open-Source Software Components

### 6.1 Licence acceptability tiers

CoinPort classifies open-source licences into four tiers. The Engineering Lead must confirm tier before any new dependency is merged.

| Tier | Description | Example licences | Approval |
| --- | --- | --- | --- |
| **A — Pre-approved** | Permissive licences with attribution-only obligations. | MIT, BSD-2-Clause, BSD-3-Clause, ISC, Apache-2.0, Unlicense, CC0-1.0, Zlib | Engineering Lead may approve. |
| **B — Conditionally approved** | Weak copyleft or notice-heavy licences that are acceptable provided the obligations are met (dynamic linking only, NOTICE preserved, source offer maintained). | LGPL-2.1, LGPL-3.0, MPL-2.0, EPL-2.0, CDDL-1.0 | Engineering Lead approves with documented compliance plan. |
| **C — Restricted** | Strong copyleft; allowed only where CoinPort does not distribute the component, does not expose it as a network service, and there is no realistic prospect of future distribution. | GPL-2.0, GPL-3.0, AGPL-3.0, SSPL-1.0, BUSL-1.1, Commons Clause, Elastic Licence v2 | CTO sign-off required, with written rationale recorded in the SBOM. |
| **D — Prohibited** | Non-OSS, "no commercial use", "no modification", custom licences with field-of-use restrictions incompatible with running an exchange, or licences with no clear grant. | CC-BY-NC, CC-BY-ND, "research only", "all rights reserved" code from blogs/Stack Overflow, JSON licence ("good not evil") | Must not be used. |

Special note on AGPL-3.0 and SSPL-1.0: because CoinPort operates a public network service, these licences are treated as **distribution-equivalent**. Tier C controls apply with particular care.

### 6.2 Procedure for adding a new dependency

Before any new library, gem, npm package, Go module, Python package, container image, or similar component is merged to a CoinPort-managed branch, the engineer introducing it must:

1. **Identify the licence.** Read the licence file in the component's repository or registry metadata. Do not rely on a label alone — open and read the actual `LICENSE`, `COPYING`, or equivalent file.
2. **Identify all transitive dependencies and their licences.** Use the SBOM tooling described in §6.4. A permissive top-level dependency that pulls a copyleft transitive dependency is itself effectively governed by the most restrictive transitive licence.
3. **Confirm the licence tier.** Match the licence to the table in §6.1. If the licence is unclear, dual-licensed, or the file is missing, treat it as **Tier D** until clarified.
4. **Check for re-licensing or licence changes.** Components that have changed licence (notably from Apache-2.0/MIT to BUSL, SSPL, or Elastic Licence — e.g. Redis, MongoDB, Elastic, HashiCorp Terraform/Vault/Consul) must be evaluated against the licence in effect at the version CoinPort uses. Pinned versions are required for any Tier B or C component.
5. **Check provenance and authorship signals.** The component must come from an official source (project repository, `rubygems.org`, `npmjs.com`, `pypi.org`, Docker Hub official image, or a verified GitHub release). Forks of unknown origin are not permitted.
6. **Check copyright notices.** Capture the copyright statement (often in the licence header or a `NOTICE` file). This must be carried forward into CoinPort's notice file (§6.5).
7. **Record the decision in the SBOM and pull request.** The PR description must list new direct dependencies with licence and tier. Merging is conditional on this record existing.

### 6.3 Procedure for upgrading an existing dependency

A version bump is treated as a new addition for licence purposes. The engineer must:

1. Re-check the licence at the new version. Re-licensing may have occurred between minor versions.
2. Re-run the SBOM (§6.4).
3. Update the notice file (§6.5) if the copyright statement, contributors, or licence has changed.

### 6.4 Software Bill of Materials (SBOM)

CoinPort maintains an SBOM for every production-deployed component:

- **Format.** CycloneDX or SPDX, generated automatically per repository.
- **Tooling.** `bundler-audit` and `licensee` for Ruby; `npm ls --all`, `license-checker` for Node; `go-licenses` for Go; `pip-licenses` for Python; `syft` for container images.
- **Frequency.** Regenerated on every CI run. The latest SBOM for each repository is stored as a build artefact and retained for the life of the repository.
- **Annual review.** The Engineering Lead reviews the consolidated SBOM annually as part of this policy's review cycle and produces a written summary of any new Tier B or C components that entered the platform during the year.

### 6.5 Notice and attribution

CoinPort preserves attribution in three locations:

1. **`LICENSE` file** at the root of every CoinPort repository. The `opendax` repository is itself under Apache-2.0 (as inherited from the upstream OpenDAX project) and that licence is preserved verbatim.
2. **`NOTICE` / `THIRD_PARTY_NOTICES.md` file** listing every third-party component, its copyright statement, and its licence. This is regenerated from the SBOM on each release.
3. **In-product attribution.** Where required by a licence (notably Apache-2.0 §4(d), BSD-3-Clause, and binary-redistributed components), the exchange UI includes a "Third-party software" or "Open source attributions" page accessible from the footer.

Removal of an upstream copyright or licence header from any source file is prohibited. Modifications to a file derived from an upstream project must be marked in accordance with the licence (e.g. Apache-2.0 §4(b) requires a "prominent notice" of modification).

### 6.6 Distribution and modification of OpenDAX

The CoinPort Exchange is a derivative of the OpenDAX stack. The following obligations apply because the upstream is Apache-2.0 (with components historically MIT and AGPL — see §6.7):

- The upstream `LICENSE` and `NOTICE` files are preserved unchanged in every fork.
- Files modified by CoinPort carry a top-of-file modification notice referencing CoinPort and the modification date, where the file already carried an upstream copyright header.
- CoinPort does not represent, in product, marketing, or documentation, that the upstream maintainers endorse or sponsor CoinPort.
- "OpenDAX", "Peatio", "Barong", "Sonic", "Tower", "Rango", and any associated upstream marks are used in a descriptive sense only (e.g. "based on OpenDAX") and never as part of a CoinPort product, service, or domain name.

### 6.7 Component-specific notes

| Component | Licence at version in use | CoinPort obligation |
| --- | --- | --- |
| OpenDAX orchestration (`opendax` repo) | Apache-2.0 | Preserve `LICENSE`, `NOTICE`; mark modified files. |
| Peatio | MIT (historical) — confirm at fork point | Preserve copyright headers; attribution in notice file. |
| Barong | Confirm at fork point | Preserve copyright headers; attribution. |
| Vault (Hashicorp) | BUSL-1.1 from v1.14.0 onwards (was MPL-2.0) | Pin to a version with a licence acceptable under §6.1. CTO sign-off required for any BUSL version. Document network-deployment posture. |
| Redis | RSALv2 / SSPL-1.0 from v7.4 (was BSD-3-Clause) | Pin to a BSD-3-Clause version, or migrate to a fork (e.g. Valkey under BSD-3-Clause). CTO sign-off required if any RSALv2/SSPL version is run. |
| MySQL community | GPL-2.0 with FOSS exception (server) / open-source connectors | Use only the database server; CoinPort does not modify or redistribute it. |
| RabbitMQ | MPL-2.0 | Standard MPL obligations; CoinPort does not modify upstream files. |
| Traefik | MIT | Attribution. |
| Envoy | Apache-2.0 | Attribution; modification notices if patched. |

This table is illustrative, not exhaustive. The authoritative list is the SBOM (§6.4).

## 7. Due Diligence — Forks and Upstream Tracking

Where CoinPort maintains a fork (under `github.com/coinport`):

1. The fork is created from a tagged upstream release, not from `main`/`master` HEAD, so that the upstream commit hash is recorded.
2. The fork's `README` records the upstream URL, the upstream commit/tag of the fork point, and the upstream licence.
3. CoinPort modifications are made on a clearly named branch (e.g. `coinport-main`) that is rebased or merged from upstream on a defined cadence (at least quarterly, security fixes immediately).
4. CoinPort modifications are marked in accordance with the upstream licence's modification-notice requirement.
5. Where the upstream relicenses, the Engineering Lead evaluates whether to (a) stay on the last permissively-licensed version, (b) migrate to a community fork, or (c) accept the new licence under §6.1. The decision is recorded.

## 8. Due Diligence — Third-Party SaaS and APIs

Each SaaS or API integration is governed by the provider's terms of service (ToS), data-processing agreement (DPA), and any developer agreement. Before integrating a new SaaS provider, the Engineering Lead and the CTO must:

1. **Read the ToS, AUP, and developer agreement.** Confirm that CoinPort's intended use (a regulated cryptocurrency exchange) is permitted. Some providers prohibit or restrict crypto, gambling, or financial-services use.
2. **Confirm trademark and brand-use rules.** Many providers (Cloudflare, Auth0, Google, Microsoft, TradingView) require specific attribution or restrict the use of their logos. Where the provider's mark is shown in the UI, follow their published brand guidelines.
3. **Confirm IP indemnity terms.** The provider's ToS should contain an IP indemnity in CoinPort's favour for the provider's outputs, and CoinPort should not have given a broad IP licence over its data beyond what is necessary to provide the service.
4. **Record the provider, the service, the contract reference, and the integration owner** in the SaaS register held with the CTO.
5. **TradingView in particular** has specific attribution and "Powered by TradingView" obligations that must be honoured exactly as specified in their licence agreement; deviation is a contractual breach and is treated as an IP issue under this policy.

Use of any AI / LLM service to generate code or content is governed by §10.6.

## 9. Due Diligence — Trademarks, Brand, Fonts, Icons, Images, and Copy

### 9.1 CoinPort marks

"CoinPort" and the CoinPort logo are CoinPort's trademarks. Marketing must:

- Avoid presenting "CoinPort" alongside an upstream mark in a way that implies sponsorship by, partnership with, or endorsement by the upstream project (OpenWare, OpenDAX, Peatio, Barong, etc.).
- Avoid using third-party marks in product or domain names. Reference to a third party for compatibility purposes ("Deposit BTC", "Sign in with Google") is nominative use and is acceptable when limited to what is necessary to identify the service.
- Avoid using the name or logo of any partner, vendor, or integration without the partner's written approval or compliance with the partner's published brand guidelines.

### 9.2 Fonts

Every font used in product, marketing, or document templates must have a written licence that covers (a) web embedding, (b) commercial use, and (c) the number of users or page views CoinPort generates. Free-tier licences from font vendors that prohibit commercial use are Tier D (§6.1) and must not be used. The licence file or licence terms are stored alongside the font file in the relevant repository.

### 9.3 Icons and illustrations

Icon sets and illustration packs must be:

- Released under an OSS or Creative Commons licence compatible with commercial use (CC0, CC-BY, MIT, Apache-2.0); **CC-BY-NC and CC-BY-ND are prohibited**.
- Licensed individually under a paid licence held in CoinPort's name with a receipt retained.

Crypto asset logos (BTC, ETH, USDT, etc.) are used in a nominative sense for the asset they identify; the logo is not modified, and the issuer's brand guidelines (where published, e.g. Tether's brand guide) are followed.

### 9.4 Images and stock photography

Every photograph, illustration, or video used in marketing or product must be one of:

- Owned by CoinPort or a CoinPort contractor under a written assignment (§10).
- Licensed from a stock provider (Shutterstock, Getty, Adobe Stock, Unsplash+, etc.) under a paid CoinPort licence; the licence proof is retained against the asset.
- Released under a public-domain or Creative Commons licence permitting commercial use; the source URL and licence are recorded against the asset.

KYC document samples and screenshots must not depict the personal documents of any real person without written consent.

### 9.5 Copy and educational content

Marketing copy, blog posts, help-centre articles, and training material must be either originally authored, licensed, or quoted under fair dealing with attribution. Use of competitor copy, exchange documentation, or third-party educational material as a source must comply with the source's terms; lifting passages of more than incidental length is prohibited.

## 10. Due Diligence — Contributions and Custom IP

### 10.1 Employees

All CoinPort employment contracts include an IP-assignment clause assigning to CoinPort all IP created by the employee in the course of their employment, together with a moral-rights consent. Onboarding is not complete until the contract is signed.

### 10.2 Contractors and agencies

Every contractor and agency engagement is governed by a written agreement that:

- Assigns to CoinPort all IP in the work product on creation (or, where assignment on creation is not possible under the relevant law, on payment).
- Warrants that the work product is original or properly licensed, and does not infringe any third-party IP.
- Requires the contractor to disclose any open-source or third-party material incorporated, with its licence.
- Includes an indemnity from the contractor for IP infringement caused by the contractor's work product.

A contractor must not start work before the agreement is signed.

### 10.3 External / open-source contributors

External contributors to CoinPort-owned repositories are accepted only when:

- The repository carries a `CONTRIBUTING.md` that sets out the licence under which contributions are accepted (typically the licence of the receiving repository, e.g. Apache-2.0 for OpenDAX-derived code).
- The contributor's pull request is signed off (`Signed-off-by`) under the Developer Certificate of Origin (DCO) **or** the contributor has signed a CoinPort Contributor Licence Agreement (CLA), depending on the repository's policy.
- Any non-trivial contribution from a contributor whose employer may have rights in the work is accompanied by written confirmation from the employer.

### 10.4 Code review for IP signals

The reviewer of every pull request (internal or external) must look for, and reject, the following:

- Code copied from Stack Overflow, blogs, tutorials, or unrelated third-party repositories without licence attribution.
- Large blocks of code introduced without provenance ("vibe-coded" or pasted from an unidentified source).
- Datasets, fixtures, or test data that resemble proprietary or personal data of third parties.
- Trademarks, logos, or copyrighted images committed to the repository without a licence record.

Suspicion of any of the above is grounds to block the PR and escalate to the CTO.

### 10.5 CoinPort-owned IP

Code, designs, and content authored by CoinPort staff and contractors are CoinPort's property. CoinPort:

- Records its copyright in headers where the file format permits.
- Tracks any internal innovation that may be patentable and refers it to the CTO for assessment before public disclosure.
- Treats its KYC workflows, risk models, alerting rules, and other internal know-how as confidential information / trade secrets and protects them accordingly.

### 10.6 Use of AI / LLM tools

AI assistants (Claude, GitHub Copilot, ChatGPT, Cursor, etc.) may be used by CoinPort engineers and content creators subject to the following:

- The engineer is responsible for the output as if they had written it. Generated code is reviewed for IP signals as in §10.4.
- The tool must be configured, where the option exists, to suppress suggestions matching public code, or the engineer must verify that any suggestion of non-trivial length is not a near-verbatim reproduction of an identifiable upstream.
- Generated content (copy, images) used in marketing must comply with §9 — the fact that an AI generated it does not eliminate any underlying IP risk.
- Confidential CoinPort information, customer data, KYC material, and unreleased internal code must not be submitted to a third-party AI service that does not contractually exclude its use for model training.

## 11. Patents

CoinPort holds no patents at the date of this policy. CoinPort takes the following posture:

- CoinPort will not knowingly practice a third-party patent without authorisation.
- CoinPort relies on the patent grants in the Apache-2.0 licence (and equivalent grants in other OSS licences) for the components it consumes, and will preserve those grants by complying with §6.
- Where CoinPort becomes aware of a patent claim that may read on CoinPort's operations, the CTO will obtain external legal advice before continuing or modifying the affected feature.
- CoinPort does not assert patents offensively.

## 12. Incident Response — IP Notices and Suspected Infringement

This section integrates with, and does not replace, the CoinPort Disaster Recovery Plan and the CoinPort Incident Response Plan.

### 12.1 Receiving a notice

Any notice received by CoinPort that asserts IP infringement — whether by email, post, DMCA-style takedown, cease-and-desist, or social media — must be:

1. Acknowledged internally by the recipient within one business day.
2. Forwarded immediately to the CTO. The recipient must not respond substantively to the sender, must not admit liability, and must not commit CoinPort to any action.
3. Logged in the IP register held with the CTO, including the sender, the asserted right, the asserted infringement, and the date received.
4. Triaged by the CTO within five business days, with external legal advice obtained where the claim is not plainly without merit.
5. Responded to within the deadline stated in the notice, on advice from external counsel.

If the asserted right is a trademark used in CoinPort's UI or marketing, the affected use is **paused immediately** pending review unless legal counsel advises otherwise.

If the asserted right is a copyright in a piece of code or content, the affected component is isolated and a remediation path (replace, relicense, remove) is identified within ten business days.

### 12.2 Discovering an internal issue

If a CoinPort engineer, contractor, or staff member discovers (or suspects) that CoinPort is using a component, asset, or piece of content outside its licence terms, they must:

1. Stop adding to the issue (no further commits, no further marketing publication).
2. Notify the Engineering Lead and the CTO the same day.
3. Cooperate in producing a timeline of how the component entered the platform.
4. Support the remediation plan agreed by the CTO.

There is no penalty for a good-faith self-report. There is a penalty for concealment.

### 12.3 Asserting CoinPort's rights

Where a third party uses CoinPort's marks, copyrighted material, or confidential information without authorisation, the CTO determines (with external legal advice) whether to send a cease-and-desist, file a takedown, or take other action. Engineers and staff must not send IP-related demands on CoinPort's behalf without CTO approval.

## 13. Recordkeeping

CoinPort maintains the following records, under the custody of the CTO, for the life of the company plus seven years:

- The SBOM history for each production repository.
- The signed CLAs / DCO sign-offs for all external contributions.
- Signed contractor and agency agreements with IP-assignment and IP-warranty clauses.
- Licences and receipts for all paid fonts, icons, illustrations, images, and stock content.
- The SaaS register, including ToS version and DPA signature dates for each provider.
- The IP-incident register, including notices received, internal discoveries, and remediation actions.
- The annual IP-policy review minutes (§14).

## 14. Training and Review

- **Onboarding.** Every new engineer, designer, and contractor receives a briefing on this policy as part of their first week. Acknowledgement is recorded.
- **Annual refresher.** All staff repeat the briefing annually. Marketing staff additionally cover §9 in detail.
- **Annual policy review.** The CTO reviews this policy at least annually (next review per the header), updating it for licence changes in the dependency stack, regulatory changes, and any incidents during the year. The review is minuted and the document version incremented.
- **Trigger reviews.** This policy is reviewed out-of-cycle when (a) a dependency in §6.7 changes licence, (b) CoinPort acquires or is acquired, (c) CoinPort begins offering a materially new product, or (d) an IP incident under §12 reveals a gap.

## 15. Enforcement

A breach of this policy is a disciplinary matter and, for contractors, a breach of contract. The severity of the response reflects the materiality of the breach: an unattributed third-party icon shipped to production is treated differently from a knowing inclusion of proprietary code. The CTO determines the response in consultation with the affected staff member's manager and, where appropriate, external counsel.

---

## Appendix A — Quick reference: adding a new dependency

1. Find the licence file. Read it.
2. Check the tier in §6.1.
3. Run the SBOM tool and check transitive dependencies.
4. Confirm the source is official (registry, project repo, verified release).
5. Capture the copyright statement for the notice file.
6. Record the licence and tier in the PR description.
7. Merge only after Engineering Lead sign-off (Tier A/B) or CTO sign-off (Tier C).

## Appendix B — Quick reference: adding a new brand asset

1. Identify the asset type (font, icon, image, copy).
2. Confirm the licence permits commercial web use.
3. Confirm the licence is **not** CC-BY-NC, CC-BY-ND, or any "no commercial use" variant.
4. Save the licence proof / receipt against the asset.
5. Record the asset, source, and licence in the brand-asset register.

## Appendix C — Quick reference: receiving an IP notice

1. Do **not** reply substantively.
2. Do **not** admit liability.
3. Forward to the CTO the same day.
4. Log it in the IP register.
5. Pause any clearly infringing use pending review.
6. Respond on advice from external counsel within the notice deadline.
