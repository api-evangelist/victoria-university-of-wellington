# Victoria University of Wellington (victoria-university-of-wellington)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Te Herenga Waka—Victoria University of Wellington is a public research university in Wellington, Aotearoa New Zealand. This repository catalogs the institution's public, machine-readable footprint as an [APIs.json](https://apisjson.org) provider profile, and its organising question is not "is there a spec" but **who operates the thing a spec describes**. A university is a federation of buyers: almost every machine-readable surface that carries this institution's name is a vendor's contract running under it. Every entry below therefore carries an `x-operator` of `institution` or `tenant`, and only `institution` contracts are saved here.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/victoria-university-of-wellington/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=victoria-university-of-wellington-api-evangelist&utm_content=repo

## Type

- university / Public Research University — Index / Consumer / 3rd-Party

## Tags

University, Higher Education, Education, New Zealand, Public Research University, Research, Open Access, Research Repository, Institutional Repository, OAI-PMH, DSpace, Library, Course Catalog, Identity Federation, Research Computing

## Domains

The institution runs three registrable domains, all resolving to the same body: `wgtn.ac.nz` (website), `vuw.ac.nz` (identity and email), `victoria.ac.nz` (library discovery). Only `wgtn.ac.nz` was recorded before this pass, which made two of its own hosts unattributable.

## Surfaces the institution operates (`x-operator: institution`)

- **Institutional Repository (self-hosted DSpace 7.6.7)** — `ir.wgtn.ac.nz`, no CNAME, resolving to 130.195.21.54 in the university's own address space, admin contact `library-systems@vuw.ac.nz`. Four keyless, anonymously callable machine-readable interfaces verified live: **OAI-PMH 2.0** at `/oai/request` (23,150 records, twelve metadata formats, sets including ResearchArchive—Te Puna Rangahau, RestrictedArchive—Te Puna Rangahau, the Stout Literary Archive and Exam Papers), a **DSpace REST** HAL+JSON root at `/server/api` (18 collections; communities and discovery search answer anonymously, `/server/api/core/items` returns 401), an **OpenSearch 1.1** description with an Atom result feed, and **FAIR Signposting** link sets carrying DataCite metadata, Handle `cite-as` and license relations. The operator is `institution` because the university runs the deployment itself — but DSpace's interfaces are open-source and identical everywhere, so the saved contract describes only the endpoints probed on this host and credits the university with operating them, never with designing them. — [OpenAPI](openapi/victoria-university-of-wellington-institutional-repository-openapi.yml)
- **Website Global Object** — public, keyless JSON configuration endpoint on the university's own CMS. HTTP 200, CORS open to all origins, `Last-Modified` 2024-04-10. Undocumented and unversioned, and it returns JSON under a `text/html` Content-Type. Base: `https://www.wgtn.ac.nz/api/globalobject` — [OpenAPI](openapi/victoria-university-of-wellington-website-globalobject-openapi.yml)
- **Shibboleth Identity Provider (Tuakiri / eduGAIN)** — SAML 2.0 IdP, entityID `https://idp.vuw.ac.nz/idp/shibboleth`, scope `vuw.ac.nz`, registered in the Tuakiri New Zealand Access Federation since 2012-06-26 with the REFEDS Research & Scholarship entity category and a REFEDS Sirtfi assurance certification. The institution's most durable machine-readable asset. — [OpenAPI](openapi/victoria-university-of-wellington-identity-federation-openapi.yml)
- **Enterprise SSO (WSO2 Identity Server)** — self-hosted at `auth-eis.vuw.ac.nz` (130.195.13.55, no CNAME), the SAML issuer behind student records. Every WSO2 discovery endpoint — OIDC, SAML2 metadata, SCIM 2.0 — returns HTTP 403 from a web application firewall. Live and protected, not absent.

## Surfaces the institution buys (`x-operator: tenant`)

The data is the university's; the contract is the vendor's. **None of these vendors' specifications are saved in this repository.**

- **Open Access Repository** — Figshare portal on the institution's own `openaccess.wgtn.ac.nz` (CNAME `figshare.com`). OAI-PMH set `portal_771`; DataCite repository `FIGSHARE.VUW`, active since 2021, 4,301 DOIs.
- **Te Waharoa Library Discovery** — Ex Libris Primo/Alma at `tewaharoa.victoria.ac.nz`, institution code `64VUW_INST`. Its SRU 1.2 endpoint is anonymously callable and returned 20,136 MARCXML records to a live probe — the largest keyless interface associated with the institution, and entirely Ex Libris's contract.
- **Nuku Learning Management** — Instructure Canvas at `nuku.wgtn.ac.nz` (CNAME `wgtn-vanity.instructure.com`); `/api/v1` answers HTTP 401.
- **Research Information System** — Symplectic Elements at `elements.wgtn.ac.nz` (CNAME `vuw.elements.symplectic.org`); HTTP 401.
- **Student Records** — Ellucian Banner Self-Service at `studentrecords.vuw.ac.nz`, self-hosted but Ellucian's contract; SAML-gated, no public interface.
- **Microsoft Entra ID tenant** — production browser sign-on; OIDC discovery and federation metadata both readable anonymously.

## Education-regime conformance

Reward-only, and every claim below is backed by a live probe recorded in [conformance](conformance/victoria-university-of-wellington-conformance.yml): `saml`, `shibboleth` and **`oai-pmh` (institution — the university's own DSpace base URL at `ir.wgtn.ac.nz/oai/request`)**; `oai-pmh` and `datacite` again as a tenant via the separate Figshare portal; `datacite` present institution-side through the repository's FAIR Signposting `describedby` relation; `lti` present via Canvas. `scim` is **unreadable rather than absent** — WSO2 ships it and the firewall returns 403. `oneroster`, `ed-fi`, `caliper`, `qti`, `crossref` were probed and not found; `orcid` is consumed by the institution, not served by it, so no credit is claimed.

## Artifacts

- [Authentication](authentication/victoria-university-of-wellington-authentication.yml) · [Scopes](scopes/victoria-university-of-wellington-scopes.yml) · [Errors](errors/victoria-university-of-wellington-errors.yml) · [Lifecycle](lifecycle/victoria-university-of-wellington-lifecycle.yml) · [Conformance](conformance/victoria-university-of-wellington-conformance.yml)
- [Repository OpenAPI](openapi/victoria-university-of-wellington-institutional-repository-openapi.yml) · [OAI-PMH Identify capture](examples/victoria-university-of-wellington-ir-oai-identify.xml) · [DSpace REST root capture](examples/victoria-university-of-wellington-ir-dspace-root.json)
- [JSON Schema](json-schema/victoria-university-of-wellington-globalobject-schema.json) · [Vocabulary](vocabulary/victoria-university-of-wellington-vocabulary.yml) · [JSON-LD context](json-ld/victoria-university-of-wellington-context.jsonld) · [Spectral rules](rules/victoria-university-of-wellington-rules.yml)
- [Plans & Pricing](plans/victoria-university-of-wellington-plans-pricing.yml) · [Rate Limits](rate-limits/victoria-university-of-wellington-rate-limits.yml) · [FinOps](finops/victoria-university-of-wellington-finops.yml) · [Domain security](security/victoria-university-of-wellington-domain-security.yml) · [Review](review.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.wgtn.ac.nz/
- GitHub (web toolkit): https://github.com/victoriauniversity
- GitHub (library): https://github.com/VUW-Library
- GitHub (research computing): https://github.com/vuw-research-computing
- Rāpoi HPC documentation: https://vuw-research-computing.github.io/raapoi-docs/
- Institutional repository: https://ir.wgtn.ac.nz/
- OAI-PMH base URL: https://ir.wgtn.ac.nz/oai/request
- Course catalogue: https://www.wgtn.ac.nz/courses
- LinkedIn: https://www.linkedin.com/school/victoria-university-of-wellington/

## Notes

**A correction was made on 2026-08-30.** The June 2026 profile of this institution saved Figshare's generic v2 REST contract into this repository as though the university had authored it, and eleven further artifacts were derived from it. That contract and every artifact derived from it — sixteen files across `openapi/`, `json-schema/`, `json-structure/`, `examples/`, `rules/`, `vocabulary/`, `json-ld/`, `collections/`, `agentic-access/` and `capabilities/` — have been removed. The Figshare relationship itself was **not** removed: it is real, and it is recorded as a tenancy. This correction lowers the institution's score, and that is the intended outcome.

**A second correction was made on 2026-08-30.** A re-run of the pipeline swept the institution's own subdomains and found `ir.wgtn.ac.nz` — a self-hosted DSpace 7.6.7 institutional repository that both the June 2026 profile and the first correction pass had missed entirely. It is the institution's largest genuinely institution-operated surface and it upgrades `oai-pmh` conformance from tenant-only to institution-operated. The university runs **two** repositories: this one, on its own infrastructure, and the Figshare portal it buys. The same sweep cleared `researcharchive.vuw.ac.nz` (302 to Te Waharoa — the legacy archive was migrated), `ecs.wgtn.ac.nz` and `homepages.ecs.vuw.ac.nz` (a Foswiki school site, HTML only), and re-confirmed that `data.wgtn.ac.nz`, `api.wgtn.ac.nz`, `courses.wgtn.ac.nz`, `timetable.wgtn.ac.nz`, `status.wgtn.ac.nz` and `developer.wgtn.ac.nz` do not resolve. This correction raises the institution's score, on its own engineering.

Everything in this profile was probed live on 2026-08-30 and no endpoint was fabricated. Two responses are easy to misread and are written down explicitly: `openaccess.wgtn.ac.nz` returns HTTP 202 with `x-amzn-waf-action: challenge` (a bot challenge — live, not dead), and the LinkedIn page returns HTTP 999 to automated probes (LinkedIn's anti-bot, resolves in a browser). No open-data portal exists (`data.wgtn.ac.nz` does not resolve), there is no `api.wgtn.ac.nz`, no `llms.txt`, and no RFC 9116 `security.txt` (`/.well-known/security.txt` returns 421). No public generative-AI policy page could be located, but the site's own search returns 403 to non-browser clients and `robots.txt` disallows `/search`, so that is a limit on our reading rather than a confirmed institutional silence.

## Maintainers

- Kin Lane — kin@apievangelist.com
