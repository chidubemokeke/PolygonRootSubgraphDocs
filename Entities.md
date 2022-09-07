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

| Field                 | Type     | Description                                 |
| --------------------- | -------- | ------------------------------------------- |
| id                    | ID!      | Checkpoint Id                               |
| Proposer              | Bytes!   | The address of the proposer                 |
| headerBlockId         | BigInt!  | The Id of the header block                  |
| checkpointNumber      | BigInt!  | The checkpoint number                       |
| reward                | BigInt!  | The reward of the proposed checkpoint       |
| start                 | BigInt!  | Start block of the proposed checkpoint      |
| end                   | BigInt!  | End block of the proposed checkpoint        |
| root                  | Bytes!   | Merkle root hash of the proposed checkpoint |
| logIndex              | String!  | LogIndex ID                                 |
| transactionHash       | Bytes!   | Transaction hash of proposed checkpoint     |
| timeStamp             | BigInt!  | The checkpoint timestamp                    |

# StateSync

Description: 

| Field                      | Type     | Description                                                |
| -------------------------- | -------- | ---------------------------------------------------------- |
| id                         | ID!      | StateSync Id                                               |
| stateId                    | BigInt!  | The stateId number                                         |
| contract                   | Bytes!   | The contract address                                       |
| syncType                   | Int!     | Type of sync                                               |
| depositorOrRootToken       | String!  | Depositor or root token address                            |
| depositedTokenOrChildToken | String!  | Address of deposited token or child token address          |
| data                       | String!  | data containing the state of the contract at sync time     |
| rawData                    | String!  | Raw data containing the state of the contract at sync time |
| logIndex                   | String!  | logIndex Id                                                |
| transactionHash            | Bytes!   | Transaction hash                                           | 
| timeStamp                  | BigInt!  | Timestamp during sync of contract state                    |
| blockNumber                | BigInt!  | Block number of the state sync                             |

# StateRegistration

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | State registration Id            |
| user                       | Bytes!   | User address                     |
| receiver                   | Bytes!   | Receiver address                 |
| sender                     | Bytes!   | Sender address                   |

# PlasmaExit

Description: 

| Field                      | Type     | Description                                                          |
| -------------------------- | -------- | -------------------------------------------------------------------- |
| id                         | ID!      | Always created using plasma-exit-${exitId}                           |
| counter                    | BigInt!  | Shows where the exitStarted transaction happened                     |
| exitId                     | BigInt!  | Exit Id                                                              |  
| exitInitiator              | Bytes!   | Address of plasma exit initiator                                     |
| exitCompleter              | Bytes!   | Address of plasma exit completed                                     |
| Token                      | Bytes!   | Token contract address                                               |
| amount                     | BigInt!  | Liquidity amount to exit                                             |
| isRegularExit              | Boolean! | Regular exit check                                                   |
| exited                     | Int!     | exit codes: 0 - exit started, 1 - exit cancelled, 2 - exit completed |
| exitStartedTxHash          | Bytes!   | Exit started transaction hash                                        |
| exitStartedTimeStamp       | BigInt!  | Exit started timestamp                                               |
| exitCancelledTxHash        | BigInt!  | Exit cancelled transaction hash                                      |
| exitCancelledTimeStamp     | BigInt!  | Exit started timestamp                                               |
| exitCompletedTxHash        | BigInt!  | Exit completed transaction hash                                      |
| exitCompletedTimeStamp     | BigInt!  | Exit started timestamp                                               |

# PredicateRegistration

Description: 

| Field                      | Type     | Description                                 |
| -------------------------- | -------- | ------------------------------------------- |
| id                         | ID!      | Predicate registration Id                   |
| tokenType                  | Bytes!   | Token contract address                      |
| predicateAddress           | Bytes!   | Predicate address                           |
| timestamp                  | BigInt!  | Predicate registration timestamp            |
| transactionHash            | Bytes!   | Transaction hash of predicate registration  |

# TokenMapping

Description: 

| Field                      | Type     | Description                         |
| -------------------------- | -------- | ----------------------------------- |
| id                         | ID!      | Token mapping Id                    |
| rootToken                  | Bytes!   | Root token address                  |
| childToken                 | Bytes!   | Child token address                 |
| tokenType                  | String!  | Token contract address              |
| isPOS                      | Boolean! | Checks wether POS is true or false  |
| timestamp                  | BigInt!  | Token mapping timestamp             |
| transactionHash            | Bytes!   | Transaction hash                    |

# FxTokenMapping

Description: 

| Field                      | Type     | Description                                    |
| -------------------------- | -------- | ---------------------------------------------- |
| id                         | ID!      | Fx token mapping Id                            |
| counter                    | BigInt!  | Fx token mapping counter                       |
| contractAddress            | Bytes!   | Contract address that handles Fx token mapping |
| rootToken                  | Bytes!   | Root token address                             |
| childToken                 | Bytes!   | Child token address                            |
| tokenType                  | String!  | Token contract address                         |
| timestamp                  | BigInt!  | Fx Token mapping timestamp                     |
| transactionHash            | Bytes!   | Fx transaction hash                            |

# FxTokenMappingCounter

Description: 

| Field                      | Type     | Description                        |
| -------------------------- | -------- | ---------------------------------- |
| id                         | ID!      | Fx token mapping Id                |
| current                    | BigInt!  | Current count for fx token mapping |

# FxDeposit

Description: 

| Field                      | Type     | Description                               |
| -------------------------- | -------- | ----------------------------------------- |
| id                         | ID!      | Fx deposit Id                             |
| counter                    | BigInt!  | Fx deposit counter                        |
| contractAddress            | Bytes!   | Contract address that handles fx deposits |
| rootToken                  | Bytes!   | Root token address                        |
| tokenType                  | String!  | Token contract address                    |
| depositor                  | Bytes!   | Address of the depositor                  |
| userAddress                | Bytes!   | User address                              |
| amount                     | BigInt!  | Amount of fx deposited in the transaction |
| tokenId                    | BigInt!  | Token Id                                  |
| timestamp                  | BigInt!  | Block timestamp                           |
| transactionHash            | Bytes!   | Fx transaction hash                       |

# FxDepositCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | Fx deposit counter Id            |
| current                    | BigInt!  | Current number of FxDeposits     |

# FxWithdraw

Description: 

| Field                      | Type     | Description                               |
| -------------------------- | -------- | ----------------------------------------- |
| id                         | ID!      | Fx withdraw Id                            |
| counter                    | BigInt!  | Fx withdraw counter                       |
| contractAddress            | Bytes!   | Contract address that handles withdrawals |
| rootToken                  | Bytes!   | Root token address                        |
| childToken                 | Bytes!   | Child token address                       |
| tokenType                  | String!  | Token contract address                    |
| userAddress                | Bytes!   | User address                              |
| amount                     | BigInt!  | Amount of fx withdrawn in the transaction |
| tokenId                    | BigInt!  | Token Id                                  |
| timestamp                  | BigInt!  | Block timestamp                           |
| transactionHash            | Bytes!   | Fx transaction hash                       |

# FxWithdrawCounter

Description: 

| Field                      | Type     | Description                      |
| -------------------------- | -------- | -------------------------------- |
| id                         | ID!      | Fx withdraw counter Id           |
| current                    | BigInt!  | Current number of FxWithdrawals  |

# Validator

Description: 

| Field                      | Type     | Description                                                      |
| -------------------------- | -------- | ---------------------------------------------------------------- |
| id                         | ID!      | Validator Id                                                     |
| validatorId                | BigInt!  | Validator Id                                                     |
| owner                      | Bytes!   | Address of the owner                                             |
| signer                     | Bytes!   | Address of the signer                                            |
| signerPubKey               | Bytes!   | Public key of the signer                                         |
| liquidatedRewards          | BigInt!  | Liquidated reward for the validator                              |
| activationEpoch            | BigInt!  | Epoch validation was activated                                   |
| deactivationEpoch          | BigInt!  | Epoch validation was deactivated                                 |
| totalStaked                | BigInt!  | Total amount of tokens staked                                    |
| selfStake                  | BigInt!  | Amount staked by the validator                                   |
| delegatedStake             | BigInt!  | Amount delegated to the validator for staking                    |
| commissionRate             | BigInt!  | Commission rate                                                  |
| nonce                      | BigInt!  | Transaction nonce                                                |
| status                     | Int!     | status codes: 0 - staked, 1 - unstaked, 2 - jailed, 3 - unjailed |
| jailEndEpoch               | BigInt!  | Epoch where validator is unjailed                                |
| auctionAmount              | BigInt!  | Auction amount                                                   |
| isInAuction                | Boolean! | Checks wether validator is in auction                            |

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

