# Notional Finance Plans

Notional Finance is a decentralized protocol and does not offer traditional SaaS pricing
tiers. Access to all APIs and subgraph endpoints is free and publicly available with no
registration or API key required.

## Protocol Access

| Access Type | Cost | Requirements |
|-------------|------|--------------|
| Subgraph API (GraphQL) | Free | None |
| Smart Contract Interaction | Gas fees only | Ethereum/Arbitrum wallet |
| TypeScript SDK | Free (open source) | None |

## On-Chain Usage Costs

Interacting with Notional Finance on-chain requires paying Ethereum or Arbitrum gas fees
for transactions. There are no protocol-level fees for reading data via the subgraph APIs.

Protocol fees (swap fees, borrowing fees) are embedded in the AMM curve and interest
rate mechanics rather than charged as explicit platform fees. These are collected by
nToken liquidity providers and the Notional DAO treasury.

## The Graph API Access

Subgraph queries via The Graph hosted service and Graph Studio are free for public
endpoints. For production applications requiring guaranteed uptime, dedicated query
capacity, or higher rate limits, operators should consider:

- Running a self-hosted Graph node
- Using The Graph Network's decentralized indexing with GRT token payment
- Contacting The Graph for enterprise SLA arrangements

## Resources

- Protocol documentation: https://docs.notional.finance/
- GitHub (open source): https://github.com/notional-finance
- Discord community: https://discord.com/invite/notional
