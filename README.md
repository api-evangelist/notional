# Notional Finance

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

Notional Finance is a fixed-rate, fixed-term DeFi lending and borrowing protocol built
on Ethereum and Arbitrum. The protocol enables users to lend and borrow crypto assets
at predetermined interest rates using fCash, a zero-coupon bond instrument representing
a fixed cash flow at maturity.

## Protocol Overview

Notional achieves fixed interest rates through its specialized AMM (Automated Market
Maker) that prices fCash tokens against underlying assets. Available tenors include
three months, six months, one year, two years, five years, ten years, and twenty years.

Key protocol components:
- **fCash**: Zero-coupon bond instrument enabling fixed-rate lending and borrowing
- **nTokens**: Liquidity provider tokens that earn fees across all fCash markets
- **Leveraged Vaults**: V3 feature enabling capital-efficient yield strategies
- **NOTE Token**: Protocol governance token

## Developer APIs

| API | Type | Network | Endpoint |
|-----|------|---------|----------|
| V2 Subgraph (Mainnet) | GraphQL | Ethereum | https://api.thegraph.com/subgraphs/name/notional-finance/mainnet-v2 |
| V3 Subgraph (Mainnet) | GraphQL | Ethereum | https://api.studio.thegraph.com/query/60626/notional-v3-mainnet/v0.0.9 |
| V3 Subgraph (Arbitrum) | GraphQL | Arbitrum | https://api.studio.thegraph.com/query/60626/notional-v3-arbitrum/version/latest |

All subgraph APIs are publicly accessible without authentication.

## Smart Contract Addresses

### Ethereum Mainnet (V2)
- Notional Proxy: `0x1344A36A1B56144C3Bc62E7757377D288fDE0369`
- NOTE Token: `0xCFEAead4947f0705A14ec42aC3D44129E1Ef3eD5`
- Wrapped fCash Factory: `0x5D051DeB5db151C2172dCdCCD42e6A2953E27261`

## Links

- Website: https://notional.finance/
- Developer Docs: https://docs.notional.finance/developer-documentation/
- V3 Technical Docs: https://docs.notional.finance/v3-technical-docs
- GitHub: https://github.com/notional-finance
- Blog: https://blog.notional.finance/
- Discord: https://discord.com/invite/notional
- Twitter: https://twitter.com/NotionalFinance

## Repository Structure

```
notional/
├── apis.yml          # APIs.json 0.19 catalog
├── README.md         # This file
├── plans/            # Pricing and access tier information
├── rate-limits/      # Rate limit documentation
└── finops/           # Cost and financial operations guidance
```
