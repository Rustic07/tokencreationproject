**Token Creation Project**

In this project,we are creating a contract using Solidity and creating several public variables and mint function to increase the total supply and also to decrease the total supply.

**Description**

For this project,we are creating two functions:-

1) The first function, we will increase the total supply by the value that we are passing and also increasing the balances by the same value.

2) In second function, we are doing just the opposite of what we have done in the first function,we are decreasing the supply by the value passed by the user.

**Getting Started**

*Excecuting Project*

We are running this project on Remix IDE which is an enviornment to execute Solidity Code.

pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public t_name="Metacrafters blockchain";
    string public t_abbr="MTB";
    uint public  t_supply= 0;
    
    // mapping variable here
    mapping (address => uint) public balances;
    
    // mint function
    function mint(address a,uint value)public
    {
    t_supply=t_supply+value;
    balances[a]=balances[a]+value;
    }

    // burn function
    function burn(address a,uint value)public
    {
    if(balances[a]>=value)
    {
    t_supply=t_supply-value;
    balances[a]=balances[a]-value;
    }
    }
}

Once the contract is deployed,we can perform the transact to check whether the program is running correctly.

**Authors**

Shrey Saverneya

**License**

This project is licensed under the MIT License

