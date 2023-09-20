# winner
# MyToken
I have created this code using the solidity programming language. The contract name is "MyToken".

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. It has been created using many functions which have been listed below
# Public variables
The code starts with assigning the name and abbreviation of the token using a string variable. The  name is token name is  'winner' and abbreviation as 'win'
# Mapping variable
The mapping of the variable is conducted in the second part of the program. This simply means that if the address is given by any user it should display back the balance amount of tokens.
# Mint function
The mint function in is used to add or generate more tokens to the total supply of that token.
# Burn function
The burn function is used to burn or destroy the tokens from the total supply. Also, an 'if statement' is provided in order to avoid burning tokens more than the total supply. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```javascript




pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public tokenName = "winner";
    string public tokenAbbrv = "win";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;
    // mint function
function mint (address _address, uint _value) public {
    
   totalSupply += _value;
   balances[_address] += _value;
}
    // burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
   totalSupply -= _value;
   balances[_address] -= _value;
  
    }
}
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can see the contract in the deployed contract section. Now copy the address from account and paste it in the address box in the mint function and put a value in the value box. Then transact it, now you can see the value in the total supply has been changed. We can do the same for the burn function.
# Author
Vishnuprasad V


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
