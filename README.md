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

Te Herenga Waka—Victoria University of Wellington is a public research university in Wellington, New Zealand, ranked #244 in the QS World University Rankings 2025. This repository catalogs the institution's public, machine-readable developer/API footprint as an [APIs.json](https://apisjson.org) provider profile. The university does not run a branded developer portal; its verifiable public footprint is standards-based scholarly and library infrastructure (Figshare Open Access repository, OAI-PMH, Ex Libris Primo/Alma discovery) plus public GitHub organizations.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/victoria-university-of-wellington/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=victoria-university-of-wellington-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Access, Library, New Zealand

## APIs

- **Open Access Repository OAI-PMH** — OAI-PMH metadata feed for the Figshare-hosted Open Access repository (set `portal_771`). Docs: https://info.figshare.com/user-guide/how-to-use-figshares-oai-pmh-service/ — Base: `https://api.figshare.com/v2/oai`
- **Figshare REST API (Open Access Repository)** — Public Figshare v2 REST API powering the university's Open Access repository. Docs: https://docs.figshare.com/ — Base: `https://api.figshare.com/v2`
- **Te Waharoa Library Discovery (Primo / Alma)** — Ex Libris Primo discovery service backed by Alma, view ID `64VUW_INST:VUWNUI`. Docs: https://www.wgtn.ac.nz/library/how-to-use-the-library/searching-for-resources
- **Website Global Object Endpoint** — Undocumented public JSON CMS config endpoint. Base: `https://www.wgtn.ac.nz/api/globalobject`

## Plans / Rate Limits / FinOps

- [Plans & Pricing](plans/victoria-university-of-wellington-plans-pricing.yml)
- [Rate Limits](rate-limits/victoria-university-of-wellington-rate-limits.yml)
- [FinOps](finops/victoria-university-of-wellington-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.wgtn.ac.nz/
- GitHub: https://github.com/victoriauniversity
- SourceCode (Library): https://github.com/VUW-Library
- LinkedIn: https://www.linkedin.com/school/victoria-university-of-wellington/
- Review: [review.yml](review.yml)

## Notes

All endpoints in this profile were probed live on 2026-06-03 and are documented in `review.yml` with their observed HTTP status. No endpoints were fabricated. The university has no centralized developer portal; the OAI-PMH and Figshare REST surfaces are operated by Figshare on the university's behalf, and the Primo discovery service is operated via Ex Libris. The `globalobject` endpoint is undocumented but publicly responsive. The LinkedIn page returns HTTP 999 to automated probes (anti-bot) but resolves in a browser. The student records portal is SSO-gated with no public API.

## Maintainers

- Kin Lane — kin@apievangelist.com
