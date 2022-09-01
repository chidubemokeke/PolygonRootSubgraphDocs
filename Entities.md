# Entities

### Entities for the Enzyme Core Subgraph are all listed below.

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
| counter                    | 



