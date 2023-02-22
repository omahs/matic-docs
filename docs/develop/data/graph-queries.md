---
id: graph-queries
title: Sample queries
sidebar_label: Querying Polygon's root subgraph
description: Learn how to use Polygon's subgraph for data
keywords:
  - docs
  - matic
  - polygon
  - the graph
  - data
  - analytics
  - index
  - indexing
  - query
image: https://matic.network/banners/matic-network-16x9.png
---

## Sample Queries

Below are some sample queries you can use to gather information from the polygon root subgraph

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

### Checkpoints

Description: This query gets the first 20 checkpoints proposed and the validated blocks assigned to it as well as the rewards for each.

```graphql
{
  checkpoints(orderBy: id, orderDirection: asc, first: 20) {
    id
    proposer
    start
    end
    checkpointNumber
    reward
    timestamp
    transactionHash
  }
}
```

### Delegators

Description: This query gets the total number of active delegators, the first 50 delegations and the validator they delegated to.

```graphql
{
  globalDelegatorCounters {
    id
    current
  }
  delegations(first: 50) {
    id
    block
    activeStake
    validatorId
  }
}
```

### Transfers

Description: This query gets the first 50 matic token transfers, the sender, receiver, value, transaction block and timestamp.

```graphql
{
  maticTransfers(first: 50, orderBy: id, orderDirection: asc) {
    id
    from
    to
    value
    block
    timestamp
  }
}
```
