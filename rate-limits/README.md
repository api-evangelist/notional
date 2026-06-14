# Notional Finance Rate Limits

Notional Finance's public subgraph APIs are hosted via The Graph protocol. Rate limits
are governed by The Graph's hosted service and Graph Studio infrastructure rather than
by Notional Finance directly.

## Subgraph API Rate Limits

### The Graph Hosted Service (V2 endpoints)
- **Requests per second**: Not publicly documented; shared infrastructure
- **Max results per query**: 1,000 entries (use `first: 1000`)
- **Default results per query**: 100 entries
- **Authentication**: None required
- **Status**: The Graph is migrating from hosted service to decentralized network

### The Graph Studio (V3 endpoints)
- **Requests per second**: Not publicly documented; subject to Graph Studio limits
- **Max results per query**: 1,000 entries (use `first: 1000, skip: N` for pagination)
- **Default results per query**: 100 entries
- **Authentication**: None required for public endpoints

## Query Pagination

For retrieving large datasets, use cursor-based or offset pagination:

```graphql
{
  accounts(first: 1000, skip: 0) {
    id
  }
}
```

Increment `skip` by 1,000 for subsequent pages until no results are returned.

## On-Chain Rate Limits

There are no rate limits for on-chain read calls (eth_call) beyond those imposed by
your RPC provider (Infura, Alchemy, etc.). Write transactions are subject to standard
Ethereum and Arbitrum mempool throughput.

## Decimal Precision

Note that Notional's subgraph data uses non-standard decimal encoding:
- Balance and portfolio values: 8 decimals (divide by 10^8)
- Interest rates and implied rates: 9 decimals (divide by 10^9)

## Resources

- Subgraph reference: https://docs.notional.finance/developer-documentation/off-chain/subgraph-reference
- V3 subgraphs: https://docs.notional.finance/v3-technical-docs/subgraph-guides/notional-v3-subgraphs
- The Graph documentation: https://thegraph.com/docs/
