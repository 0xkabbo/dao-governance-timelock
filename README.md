# DAO Governance Timelock

A robust, flat-structure implementation of a Decentralized Autonomous Organization (DAO). This repository provides the framework for community-led decision-making where proposals are subject to a time-delayed execution.

## Governance Flow
1. **Proposal**: A token holder submits a proposal (e.g., to transfer funds or change a parameter).
2. **Voting**: Holders of the `GovToken` cast votes (For, Against, or Abstain).
3. **Queue**: If the proposal passes (reaches quorum and majority), it is moved to the Timelock.
4. **Execution**: After a 2-day delay, anyone can trigger the execution of the proposal.



## Key Features
* **Quorum Sensing**: Ensures a minimum percentage of total supply participates.
* **Timelock Security**: Prevents "flash" changes, giving users time to exit if they disagree with a passed proposal.
* **Delegation**: Supports ERC20Votes for gas-efficient vote delegation.

## Setup
1. Deploy `GovernanceToken.sol`.
2. Deploy `TimelockController.sol`.
3. Deploy `GovernorContract.sol` using the token and timelock addresses.
4. Transfer ownership of the protocol/funds to the Timelock.
