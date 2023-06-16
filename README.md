
# Create a Token

This Solidity program helps to create a token which can be minted i.e. created and burned i.e. destroyed. The purpose of this program is to demonstrate the functionality of Solidity programming language through the use of variables, mapping, functions and conditional statements.


## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has three state variables that store the token name, token abbrv. and the total supply. There is a mapping that stores the address of the contract and the amount of tokens that it has. Further, there are two functions. The "mint" function increases the total supply of tokens and the amount of balance the respective address holds. The other function i.e. "burn" decreases the total supply and the amount of balance the respective address holds. This program serves as a simple way to create a token, mint it and even burn it i.e. destroy it using the Solidity programming language.


## Getting Started
**Executing program**

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., EthAssessment.sol). Copy and paste the following code into the file:

    pragma solidity 0.8.7;
    contract MyToken {

        // public variables here
        string public tokenName = "Learner";
        string  public tokenAbbrev  = "LR";
        uint public totalSupply  = 0;

        // mapping variable here
        mapping (address => uint) public balances; //the address returns the token amt that addr ha

        // mint function
        function  mint(address _addr, uint _value) public{
            totalSupply += _value;
            balances[_addr] += _value;
        }

        // burn function
        function  burn(address _addr, uint _value) public{
            if(balances[_addr] >= _value){
                totalSupply -= _value;
                balances[_addr] -= _value;
            }
        }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.7" (or another compatible version), and then click on the "Compile EthAssessment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "EthAssessment" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function or burn function or adding values to balances mapping. Click on the "EthAssessment" contract in the left-hand sidebar, and then click on the "mint" function. Then add the values for "_addr" and "_value". Finally, click on the "transact" button to execute the function. Similarly, perform for "burn" function and for "balances" mapping add an address and then click on "call".


## Authors

- [@Isheta20](https://github.com/Isheta20)
- [Metacrafters](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see [MIT LICENSE](https://github.com/Isheta20/ETHAssessement/blob/main/LICENSE)
 for details

