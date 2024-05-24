
# Project: Smart Contract

This solidity smart contract is intended to create, manage, and utulize the features of a basic token system known as CoinToken(CT). It allows for the minting which we add token and burning which remove our tokens. 

# Getting Started

### Executing the program 
 I use remix: https://remix.ethereum.org/ to make this program.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

```
- **SPDX-License-Identifier: MI** : Indicates the licensed
- **pragma solidity 0.8.25;** : Solidity Version

## Mapping Variable 
```solidity
mapping(address => uint) public balances;

```
- A variable that associates Ethereum addresses and the token balances.
  
# Functions

## Mint Function 

```solidity
function mint(address addr, uint _amount) public {
    totalSupply += _amount;  
    balances[addr] += _amount;
}
```
- This mint function is initialized to allows the contract owner to mint or add specified amount and assign them to a specific address

## Burn Function 
```solidity
function burn(address addr, uint _amount) public {
    if (balances[addr] >= _amount)
    totalSupply -= _amount;
    balances[addr] -= _amount;  
}
```
- This burn function is initialized to allows the contract owner to burn or remove new tokens and assign them from a specific address 

## License
This project is licensed under the MIT License - see the LICENSE.md file for details

