# Paapi Token (EMT)

Paapi Token (EMT) is a simple ERC-20 compatible token implemented on the Ethereum blockchain. This contract allows for token minting and burning functionalities.

Contract Details
Public Variables
Token Name: EarthMeta
Token Abbreviation: EMT
Total Supply: 0 (initially)

## Description

The Paapi_token contract is a basic implementation of a cryptocurrency token on the Ethereum blockchain. This contract, written in Solidity, allows the creation, management, and destruction of tokens. The key features include:

*Public Variables: The contract stores the token's name (EarthMeta), abbreviation (EMT), and total supply. *Address Balances: A mapping of addresses to their respective token balances, allowing for easy tracking and management of token holdings. *Mint Function: Enables the creation of new tokens. When invoked, it increases the total supply and allocates the specified number of tokens to a given address. *Burn Function: Allows for the destruction of tokens. It decreases the total supply and the balance of the specified address, ensuring that the address has enough tokens to burn before performing the operation.

This contract provides a foundational framework for developing a token system, which can be further expanded with additional features and functionalities as needed.
## Getting Started

### Installing

To download the code, you can visit the following file path:-
https://github.com/Paaapi/assessment_1.sol/blob/main/assessment_1.sol

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at
code blocks for commands
```
(https://remix.ethereum.org/.)

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Meta.sol). Copy and paste the following code into the file: contract MyToken {
```
contract Paapi_token{

     // public variables here
    string public tokenName = "EarthMeta";
    string public tokenAbb = "EMT";
    uint public totalSupply = 0;

 // mapping variable here
    mapping(address=>uint) public paap;

    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        paap[_address] += _value;

    }
    // burn function
    function burn(address _address, uint _value) public{
        if(paap[_address]>= _value){
            totalSupply -= _value;
            paap[_address] -= _value;
        } 

    }
}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile Meta.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you will set the value and address in right side under the MyToken contract. After initializing the value use the function mint and burn to check the working of code.

command to run if program contains helper info
```

## Authors

Paravdeep Walia(@paravdeep_walia

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
