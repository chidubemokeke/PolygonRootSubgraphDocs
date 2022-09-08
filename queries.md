---
sidebar_position: 3
title: Sample Queries
---

## Sample Queries
Below are some sampl queries you can use to gather information from polygon root subgraph

You can build your own queries using a [GraphQL Explorer](https://graphiql-online.com/graphiql) and enter your endpoint to limit the data to exactly what you need.

### Checkpoints

Description: Get checkpoints proposed and the validated blocks assigned to it as well as the rewards for each.

```graphql
{
  checkpoints(orderBy: id, orderDirection: asc) {
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

Description: Get total number of active delegators, their delegations and the validator they delegated to.

```graphql
{
  globalDelegatorCounters {
    id
    current
  }
	delegations {
    id
    block
    activeStake
    validatorId
  }
}
```
