
# Project: Smart Contract

This solidity smart contract is intended to create, manage, and utulize the features of a basic token system known as CoinToken(CT). It allows for the minting for creating or adding token and burning removed tokens.

# Getting Started

### Executing the program 
 I use remix: https://remix.ethereum.org/ to make this program.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

```
- **SPDX-License-Identifier: MI** : Indicates the lincense
- **pragma solidity 0.8.25;** : Specify the Version

We call our variable "Meta" as a contract that allows the user to mint and burn tokens. This contract contains public variables, a mapping , and functions for mining and burning tokens. 

## Public Variables 
```solidity
contract MyToken {

    // public variables here
    string public tokenName = "Meta";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;
```
- the public variables represent the tokenName with a value of "Meta", with its abbreviation of "MTA", and lastly, the total supply with a value of 0 

## Mapping Variable 
```solidity
 // mapping variable here
 mapping(address => uint) public balances;

```
- A variable that associates Ethereum addresses with their token balances.
  
# Functions

## Mint Function 

```solidity
    // mint function
    function mint (address _address, uint _value) public  {
        totalSupply += _value;
        balances[_address] += _value;
}
```
- This mint function allows the contract owner to mint or add specified amount and assign them to a specific address

## Burn Function 
```solidity
    // burn function
    function burn (address _address, uint _value) public  {
        if (balances[_address] >= _value)
            totalSupply -= _value;
            balances[_address] -= _value;
    } 
```
- This burn function allows the contract owner to burn or remove new tokens and assign them from a specific address 

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
