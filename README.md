# Notional Finance

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
