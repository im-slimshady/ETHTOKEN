# ETHTOKEN

This is a token project created for our course in Metacrafters.

## Description
This program is a Solidity-based smart contract. The contract has a function that increases the total supply and balance of the address by a specified amount of value. The other function is to deduct the value from the total supply and the address' balance.

## Getting Started
### Executing program
Remix is an online Solidity IDE that you may use to run this application. To get started, go to https://remix.ethereum.org/.

When you are on the Remix website, click the "file" button in the left-hand sidebar to create a new file. The file should be saved with a.sol extension (such as ethToken.sol). You can copy and paste the code below into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

       string public tokenName = "ETHEREUM";
       string public tokenAbbrv = "ETH";
       uint public totalSupply = 0;

       mapping(address => uint) public balances;

       function mint (address _address, uint _value) public {
           totalSupply += _value;
           balances[_address] += _value; 
       }

       function burn (address _address, uint _value) public {
           if (balances[_address] >= _value){
           totalSupply -= _value;
           balances[_address] -= _value;
       } 
    }       
}
```
Click the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Click the "Compile ethToken.sol" button after making sure the "Compiler" option is set to "0.8.18" (or another compatible version).

With the "Deploy & Run Transactions" tab in the left-hand sidebar, you can deploy the contract after the code has been compiled. Click the "Deploy" button after selecting the "ethToken" contract from the drop-down menu. You can view the deployed contracts below the left-side hand bar once the contract has been deployed. Press the "ETHTOKEN" contract. 

To execute the mint function, click the arrow down button on the right of the mint button to enter the value you wish to mint. After inserting the value, copy the address from the "ACCOUNT" right-hand sidebar at the top, and paste it into the "_address" area.You can now click the "transact" button to get the total supply and to call the balance. Same execution for the burn function as for the mint function, but different results.

## Author
NTC Lanz

[@im-slimshady](https://github.com/im-slimshady)
