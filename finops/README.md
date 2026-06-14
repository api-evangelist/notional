# Notional Finance FinOps

This document outlines cost considerations for integrating with Notional Finance APIs
and the broader protocol infrastructure.

## API Cost Summary

| Component | Cost Model | Estimated Cost |
|-----------|-----------|----------------|
| Subgraph read queries (V2) | Free (hosted service) | $0 |
| Subgraph read queries (V3) | Free (Graph Studio) | $0 |
| TypeScript SDK | Free (open source) | $0 |
| On-chain reads (eth_call) | RPC provider dependent | $0–varies |
| On-chain write transactions | Gas fees | Variable (Ethereum/Arbitrum) |

## Gas Cost Considerations

All state-changing interactions with Notional Finance smart contracts require gas:

### Ethereum Mainnet (V2)
- Lending/borrowing transactions: High gas usage due to AMM calculations and fCash minting
- nToken minting/redeeming: Moderate gas usage
- Leveraged vault entry/exit: Higher gas due to multi-step transactions
- Typical range: 150,000–400,000 gas units per transaction

### Arbitrum One (V3)
- Significantly lower gas costs than Ethereum mainnet
- Typical range: Comparable operations cost ~10–50x less than Ethereum mainnet
- Recommended deployment for cost-sensitive integrations

## RPC Provider Costs

Querying on-chain data requires an RPC endpoint:
- **Free tier providers**: Infura (100K req/day), Alchemy (300M compute units/month), QuickNode
- **Self-hosted**: Run own Ethereum/Arbitrum node (higher infrastructure cost, unlimited queries)

## The Graph Decentralized Network

If migrating from hosted service to The Graph Network:
- Queries are paid in GRT (The Graph's native token)
- Cost per query varies based on indexer competition and query complexity
- Budget allocation: Estimate $0.0001–$0.001 per query at current GRT prices

## Protocol Revenue (not a cost to API consumers)

Notional Finance generates protocol revenue through:
- Swap fees collected by liquidity AMM (embedded in fCash pricing)
- Reserve fees accruing to the Notional DAO treasury
- nToken portfolio management fees

These fees are paid by borrowers/lenders using the protocol, not by API data consumers.

## Cost Optimization Tips

1. **Use Arbitrum V3** for transaction-heavy applications to reduce gas costs
2. **Batch subgraph queries** using GraphQL to minimize round trips (max 1,000 results/query)
3. **Cache subgraph data** locally for read-heavy analytics workloads
4. **Use free RPC tiers** for development; upgrade to paid tiers for production volume
5. **Monitor The Graph migration** from hosted service to decentralized network

## Resources

- Protocol fee documentation: https://docs.notional.finance/notional-v2
- V3 technical docs: https://docs.notional.finance/v3-technical-docs
- Gas tracker (Ethereum): https://etherscan.io/gastracker
- Gas tracker (Arbitrum): https://arbiscan.io/gastracker
