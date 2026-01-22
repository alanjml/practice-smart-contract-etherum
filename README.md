# practice-smart-contract-etherum
this repo is a practice solidity skills

##First smart contract practice

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

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

contract Mappingpractice {
    // Declare a state variable to save the value, Mapping from address to uint
   // mapping(address => uint256) public myMap;
    mapping(address => string) private students;
    //Declare a function to set value for a student
    function setStudent (address _addr, string memory _name)public {
        students[_addr] = _name;
    }

    // declare a function to show/get the value from state variable
    function getStudent (address _addr) public view returns (string memory){
        return students[_addr];
    }

    // declare a function to delete a studsent
    function removeStudent(address _addr) public {
        delete students[_addr];
    }
}
```
