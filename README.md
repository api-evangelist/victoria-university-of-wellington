# Victoria University of Wellington (victoria-university-of-wellington)

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
