# AnyVision

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

AnyVision Interactive Technologies is an Israeli computer-vision company that rebranded as **Oosto** in
October 2021 and was acquired by **Metropolis Technologies** in January 2025 for USD 125M. It builds
real-time facial recognition and video analytics ("Vision AI") for physical security and access
control, sold as three products: **Oosto OnWatch** (real-time watchlist alerting and person-of-interest
monitoring against live camera feeds), **Oosto OnAccess** (touchless facial access control, tailgating
detection, visitor management), and **Oosto Protect** (cloud alerting). The platform is deployed on
premises, at the edge on a Vision AI Appliance, on smart cameras via embedded SDKs, or in the cloud,
and integrates with third-party VMS and access-control systems including Milestone, Genetec and
Honeywell.

## API surface

There is **no public, vendor-hosted API**. Both product APIs ship with the customer's own on-premise
installation, and the reference documentation sits behind an email one-time-password login at
`knowledge.oosto.com`. No OpenAPI, AsyncAPI, GraphQL SDL, MCP server or A2A agent card is published on
any Oosto host. The operations recorded in this profile were recovered from the vendor's own **public
sample code** at [AnyVisionltd/oosto-api-sample-code](https://github.com/AnyVisionltd/oosto-api-sample-code):

- **Oosto OnWatch** — REST + Socket.IO under `/bt/api`; bearer JWT from `POST /bt/api/login` (with a
  `POST /bt/api/eula` acknowledgement gate), offset/limit paged reads, and a `track:created` detection
  event stream on `/bt/api/socket.io`.
- **Oosto OnAccess** — REST under `/abx/api`; bearer JWT login, multipart face-feature extraction at
  `POST /abx/api/external-functions/extract-faces-from-image`, and member enrolment at
  `POST /abx/api/members`.

## Links

- https://oosto.com/
- https://github.com/AnyVisionltd
- https://knowledge.oosto.com/docs (login required)
- https://forgeglobal.com/anyvision_stock/
