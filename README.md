# Lottery Smart Contract

This is a smart contract written in Solidity version ^0.8.0 for a simple lottery system.

## Contract Overview

The `Lottery` contract allows users to participate in a lottery by betting a specified amount of ether. The contract maintains the following state variables and functions:

- **State Variables**:
  - `players`: An array to store the addresses of all participating players.
  - `currentState`: An enum indicating the current state of the lottery (`IDLE` or `BETTING`).
  - `betCount`: The number of bets allowed in each round.
  - `betSize`: The size of each bet in wei.
  - `houseFee`: The percentage of the house fee.
  - `admin`: The address of the contract admin.

- **Functions**:
  - `createBet(uint count, uint size)`: Allows the admin to create a new bet with a specified count and size.
  - `bet() payable`: Allows users to place bets by sending ether to the contract.
  - `cancel()`: Allows the admin to cancel the bet and refund all players.
  - `_randomModulo(uint modulo)`: Internal function to generate a random number within a specified modulo.
  
## Frontend Overview

The frontend application interacts with the `Lottery` smart contract to allow users to participate in the lottery. It provides the following features:

- Displaying current state of the lottery (IDLE or BETTING).
- Displaying house fee percentage.
- Creating a new bet with specified count and size.
- Placing bets.
- Cancelling the current bet by the admin.

## How to Use

1. Deploy the `Lottery` smart contract to a supported Ethereum network.
2. Connect the frontend application to the deployed contract address.
3. Interact with the frontend to create bets, place bets, and cancel bets as necessary.

### Frontend Deployment Instructions

1. Clone the repository containing the frontend code.
2. Install dependencies using `npm install`.
3. Configure the `Lottery` contract address in the frontend code.
4. Run the frontend application using `npm start`.

## Note

Ensure that you have a compatible Ethereum wallet (such as MetaMask) installed and connected to the supported network to interact with the lottery contract.

