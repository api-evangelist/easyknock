# EasyKnock

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

EasyKnock was a New York based residential real estate fintech, founded in 2016 by Jared Kessler,
that pioneered consumer sale-leaseback in the United States: homeowners sold their house to
EasyKnock for cash and stayed on as renting tenants with an option to repurchase. The company
raised roughly $430 million in equity and debt and rolled up several proptech businesses —
Ribbon Home, Onder, Balance Home, HomePace and FarmlandFinder — before consumer lawsuits and
state attorney general and regulator actions in Massachusetts, Michigan, Connecticut, Texas,
Maryland, South Carolina, Pennsylvania and Ohio over its sale-leaseback disclosures.

**EasyKnock announced it had closed its doors on December 6, 2024.**

## Why this profile is thin

`easyknock.com` still returns HTTP 200, but the entire site is one static paragraph —
"After many years of serving consumers, EasyKnock has closed its doors" — served out of a
Google Cloud Storage bucket. There is no navigation and there are no links of any kind. The
legacy API host `api.easyknock.com` still has a Cloudflare DNS record but answers HTTP 530 /
`error code: 1016` (Origin DNS error), meaning the origin behind it has been deleted.

Full contract discovery was run anyway before recording the zero — OpenAPI, Swagger, GraphQL,
AsyncAPI, MCP, `llms.txt` and the whole `/.well-known/` surface across all three hosts, plus
GitHub and the npm / PyPI / RubyGems / crates.io registries. Every probe missed. The recorded
absences are in [`well-known/easyknock-well-known.yml`](well-known/easyknock-well-known.yml).

The one artifact with real content is
[`security/easyknock-domain-security.yml`](security/easyknock-domain-security.yml): the domain
is still registered and still publishes SPF and a DMARC `quarantine` policy, consistent with a
wind-down that keeps email working for former customers.

- Website (shutdown notice): https://www.easyknock.com/
- Secondary-market listing: https://forgeglobal.com/easyknock_stock/
