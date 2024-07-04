<h1 align="center">ETH + AVAX PROOF: Intermediate EVM Course</h1>
<h1 align="center">Project: Create and Mint Token</h1>

# MyToken Smart Contract

## Overview

The `MyToken` contract is an implementation of an ERC20 token using the OpenZeppelin library. This contract includes functionalities for the contract owner to mint tokens, and for any user to transfer or burn tokens.

## Features

- **Mint Tokens**: The contract owner can mint new tokens to a specified address.
- **Transfer Tokens**: Users can transfer tokens to another address.
- **Burn Tokens**: Users can burn their own tokens.

## Contract Details

### Minting Tokens

- **Function**: `ownerMintToken(address recipient, uint256 qtyToken)`
- **Description**: Allows the contract owner to mint new tokens and assign them to a specified address.
- **Modifiers**: `exclusiveOwner` ensures that only the contract owner can call this function.
- **Events**: Emits a transfer event as per the ERC20 standard when tokens are minted.

### Transferring Tokens

- **Function**: `userTransferToken(address recipient, uint256 qtyToken)`
- **Description**: Allows any user to transfer tokens to another address.
- **Return Value**: Returns `true` upon successful transfer.
- **Events**: Emits a transfer event as per the ERC20 standard.

### Burning Tokens

- **Function**: `userBurnToken(uint256 qtyToken)`
- **Description**: Allows any user to burn their own tokens, reducing the total supply.
- **Events**: Emits a burn event as per the ERC20 standard.

## Error Handling

### `require(condition, message)`

- **Usage**: Ensures that only the contract owner can call the `ownerMintToken` function.
- **Effect**: If the caller is not the contract owner, the function execution will revert with the message "Caller is not the owner".

## Solidity Version

This contract is written in Solidity version ^0.8.0.

## Usage

To deploy and interact with the contract:
- Compile and deploy in the remix IDE and interact with the contract.

## Authors

Contributors names and contact info

- Clint Audrey Dela Cruz
- Github: SecreShall
