# practice-smart-contract-etherum
this repo is a practice solidity skills

##First snart contract practice

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

//this is the contract to hash strings using keccak256
contract AlanHashingString {
//declare state variable
    bytes32 private alanString;
//hashing the string
    function hashing (string memory _str) public {
    alanString = keccak256(bytes(_str));
    }
//get the digest of the hashing process
    function getHashResult () public view returns (bytes32) {
    return alanString;
    }
}

```
