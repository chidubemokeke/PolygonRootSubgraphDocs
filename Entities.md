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
| start
