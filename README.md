## السلام عليكم ورحمة الله وبركاته 
## May Allah's peace, mercy and blessings be upon you!
**This is my first smart contract.**

Used in:
-   **Solidity**: is a high-level programming language used for developing smart contracts on the Ethereum blockchain.
-   **Foundry**:  is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust 

## Documentation for Foundry

https://book.getfoundry.sh/

**code**

```solidity
// I'm a comment!
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

// pragma solidity ^0.8.0;
// pragma solidity >=0.8.0 <0.9.0;

contract SimpleStorage {
    uint256 myFavoriteNumber;

    struct Person {
        uint256 favoriteNumber;
        string name;
    }
    // uint256[] public anArray;
    Person[] public listOfPeople;

    mapping(string => uint256) public nameToFavoriteNumber;

    function store(uint256 _favoriteNumber) public virtual {
        myFavoriteNumber = _favoriteNumber;
    }

    function retrieve() public view returns (uint256) {
        return myFavoriteNumber;
    }

    function addPerson(string memory _name, uint256 _favoriteNumber) public {
        listOfPeople.push(Person(_favoriteNumber, _name));
        nameToFavoriteNumber[_name] = _favoriteNumber;
    }
}
```
