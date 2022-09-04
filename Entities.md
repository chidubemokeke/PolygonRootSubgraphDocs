# Entities

### Entities for the Polygon Root Subgraph are all listed below.

- Checkpoint
- StateSync
- StateRegistration
- PlasmaExit
- PredicateRegistration
- TokenMapping
- FxTokenMapping
- FxTokenMappingCounter
- FxDeposit
- FxDepositCounter
- FxWithdraw
- FxWithdrawCounter
- Validator
- StakeUpdate
- GlobalDelegatorCounter
- GlobalPlasmaExitCounter
- Delegator
- Topup
- StakingParams
- StakingNFTTransfer
- DelegatorUnbond
- MaticTransfer
- GlobalDelegationCounter
- Delegation

# Checkpoint

Description:

| Field                 | Type     | Description                      |
| --------------------- | -------- | -------------------------------- |
| id                    | ID!      | ID is set to 1                   |
| Proposer              | Bytes!   |                                  |
| headerBlockId         | BigInt!  |                                  |
| checkpointNumber      | BigInt!  |                                  |
| reward                | BigInt!  |                                  |
| start                 | BigInt!  |                                  |
| end                   | BigInt!  |                                  |
| root                  | Bytes!   |                                  |
| logIndex              | String!  |                                  |
| transactionHash       | Bytes!   |                                  |
| timeStamp             | BigInt!  |                                  |

# StateSync

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| stateId                    | BigInt!  |                                  |
| contract                   | Bytes!   |                                  |
| syncType                   | Int!     |                                  |
| depositorOrRootToken       | String!  |                                  |
| depositedTokenOrChildToken | String!  |                                  |
| data                       | String!  |                                  |
| rawData                    | String!  |                                  |
| logIndex                   | String!  |                                  |
| transactionHash            | Bytes!   |                                  | 
| timeStamp                  | BigInt!  |                                  |
| blockNumber                | BigInt!  |                                  |

# StateRegistration

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| user                       | Bytes!   |                                  |
| receiver                   | Bytes!   |                                  |
| sender                     | Bytes!   |                                  |

# PlasmaExit

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| exitId                     | BigInt!  |                                  |
| exitInitiator              | Bytes!   |                                  |
| exitCompleter              | Bytes!   |                                  |
| Token                      | Bytes!   |                                  |
| amount                     | BigInt!  |                                  |
| isRegularExit              | Boolean! |                                  |
| exited                     | Int!     |                                  |
| exitStartedTxHash          | Bytes!   |                                  |
| exitStartedTimeStamp       | BigInt!  |                                  |
| exitCancelledTxHash        | BigInt!  |                                  |
| exitCancelledTimeStamp     | BigInt!  |                                  |
| exitCompletedTxHash        | BigInt!  |                                  |
| exitCompletedTimeStamp     | BigInt!  |                                  |

# PredicateRegistration

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| tokenType                  | Bytes!   |                                  |
| predicateAddress           | Bytes!   |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# TokenMapping

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| rootToken                  | Bytes!   |                                  |
| childToken                 | Bytes!   |                                  |
| tokenType                  | String!  |                                  |
| isPOS                      | Boolean! |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# FxTokenMapping

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| contractAddress            | Bytes!   |                                  |
| rootToken                  | Bytes!   |                                  |
| childToken                 | Bytes!   |                                  |
| tokenType                  | String!  |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# FxTokenMappingCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  |                                  |

# FxDeposit

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| contractAddress            | Bytes!   |                                  |
| rootToken                  | Bytes!   |                                  |
| tokenType                  | String!  |                                  |
| depositor                  | Bytes!   |                                  |
| userAddress                | Bytes!   |                                  |
| amount                     | BigInt!  |                                  |
| tokenId                    | BigInt!  |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# FxDepositCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  | Current number of FxDeposits     |

# FxWithdraw

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| contractAddress            | Bytes!   |                                  |
| rootToken                  | Bytes!   |                                  |
| childToken                 | Bytes!   |                                  |
| tokenType                  | String!  |                                  |
| userAddress                | Bytes!   |                                  |
| amount                     | BigInt!  |                                  |
| tokenId                    | BigInt!  |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# FxWithdrawCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  | Current number of FxWithdrawals  |

# Validator

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| validatorId                | BigInt!  |                                  |
| owner                      | Bytes!   |                                  |
| signer                     | Bytes!   |                                  |
| signerPubKey               | Bytes!   |                                  |
| liquidatedRewards          | BigInt!  |                                  |
| activationEpoch            | BigInt!  |                                  |
| deactivationEpoch          | BigInt!  |                                  |
| totalStaked                | BigInt!  |                                  |
| selfStake                  | BigInt!  |                                  |
| delegatedStake             | BigInt!  |                                  |
| commissionRate             | BigInt!  |                                  |
| nonce                      | BigInt!  |                                  |
| status                     | Int!     |                                  |
| jailEndEpoch               | BigInt!  |                                  |
| auctionAmount              | BigInt!  |                                  |
| isInAuction                | Boolean! |                                  |

# StakeUpdate

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| validatorId                | BigInt!  |                                  |
| totalStaked                | BigInt!  |                                  |
| block                      | BigInt!  |                                  |
| nonce                      | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |
| logIndex                   | BigInt!  |                                  |

# GlobalDelegatorCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  | Current number of delegators     |

# GlobalPlasmaExitCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  | Current number of plasma exits   |

# Delegator

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| validatorId                | BigInt!  |                                  |
| address                    | Bytes!   |                                  |
| delegatedAmount            | BigInt!  |                                  |
| unclaimedAmount            | BigInt!  |                                  |
| claimedAmount              | BigInt!  |                                  |
| tokens                     | BigInt!  |                                  |
| claimedRewards             | BigInt!  |                                  |

# Topup

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| address                    | Bytes!   |                                  |
| topupAmount                | BigInt!  |                                  |
| withdrawAmount             | BigInt!  |                                  |

# StakinParams

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| owner                      | Bytes!   |                                  |
| validatorThreshhold        | BigInt!  |                                  |
| prosperBonus               | BigInt!  |                                  |
| dynasty                    | BigInt!  |                                  |
| liquidatedRewards          | BigInt!  |                                  |

# StakingNFTTransfer

Description: 

| Field                      | Type      | Description                      |
| -------------------------- | --------- | -------------------------------- |
| id                         | ID!       | ID is set to 1                   |
| tokenId                    | BigInt!   |                                  |
| currentOwner               | Bytes!    |                                  |
| previousOwners             | [Bytes!]! |                                  |
| transactionHashes          | [Bytes!]! |                                  |

# DelegatorUnbond

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| nonce                      | BigInt!  |                                  | 
| validatorId                | BigInt!  |                                  |
| user                       | Bytes!   |                                  |
| amount                     | BigInt!  |                                  |
| tokens                     | BigInt!  |                                  |
| completed                  | Boolean! |                                  |
| unbondStartedTXHash        | Bytes!   |                                  |
| unbondStartedTimeStamp     | BigInt!  |                                  |
| unbondClaimedTXHash        | Bytes!   |                                  |
| unbondClaimedTimeStamp     | BigInt!  |                                  |
| activeStake                | BigInt!  |                                  |

# MaticTransfer

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| token                      | Bytes!   |                                  |
| from                       | Bytes!   |                                  |
| to                         | Bytes!   |                                  |
| value                      | BigInt!  |                                  |
| block                      | BigInt!  |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |

# GlobalDelegationCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| current                    | BigInt!  | Current number of delegations    |

# Delegation

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | ID is set to 1                   |
| counter                    | BigInt!  |                                  |
| validatorId                | BigInt!  |                                  |
| address                    | Bytes!   |                                  |
| timestamp                  | BigInt!  |                                  |
| transactionHash            | Bytes!   |                                  |
| amount                     | BigInt!  |                                  |
| block                      | BigInt!  |                                  |
| activeStake                | BigInt!  |                                  |

