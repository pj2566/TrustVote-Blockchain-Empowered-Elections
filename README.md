# README for Decentralized Voting Project

## Overview

The Decentralized Voting Project is a blockchain-based voting system implemented using Solidity. It allows for transparent and secure voting on the Ethereum blockchain. The project consists of a main smart contract (`Voting.sol`) and a deployment script (`deploy.js`).

## Voting.sol

### Features

-   **Candidate Management**: Allows adding candidates with their names and tracking their vote counts.
-   **Ownership**: The contract is owned by the creator, who can add candidates.
-   **Voting Mechanism**: Registered candidates can be voted on by any Ethereum address.
-   **Vote Tracking**: Ensures that each Ethereum address can vote only once.
-   **Voting Period Control**: Voting starts and ends at predefined times.
-   **Voting Status and Results**: Functions to check the ongoing status of voting and to get the total votes for each candidate.

### Functions

-   `constructor`: Initializes the contract with a list of candidates and sets the voting duration.
-   `addCandidate`: Adds a new candidate to the list (only callable by the owner).
-   `vote`: Records a vote for a specified candidate.
-   `getAllVotes`: Returns the list of all candidates and their vote counts.
-   `getVotingStatus`: Checks if the voting is currently active.
-   `getRemainingTime`: Provides the remaining time for the voting to end.
-   `delegate`: Enables a voter to delegate their vote to another address.
-   `delegateTo`: Returns the address to which a particular voter has delegated their vote.

## deploy.js

This Node.js script deploys the `Voting` contract to the Ethereum blockchain. It utilizes Hardhat, a development framework for Ethereum.

### Usage

1. Ensure that you have Hardhat and other dependencies installed.
2. Run the script to deploy the contract:
    ```shell
    node scripts/deploy.js
    ```

### Deployment Process

-   The script deploys the `Voting` contract to the specified Ethereum network.
-   It initializes the contract with predefined candidate names and a voting duration.
-   Outputs the deployed contract address.

## Installation

1. Clone the repository.
2. Install dependencies:
    ```shell
    npm install
    ```
3. Set up your environment with Hardhat configurations.

## Requirements

-   Node.js
-   Hardhat
-   Ethereum wallet with testnet/mainnet ETH for deployment.

---

## Testing

### Running Tests

To run the automated test suite:

```shell
npx hardhat test

Note: The README provides a basic overview of the project. For more detailed information about the code and its deployment, refer to the inline comments within the contract and the deployment script.
```
