# Developing applications with Ethereum Blockchain

# 1. Introduction

# 2. Ethereum Protocol

## 2.1 Introduction

Decentralized Applications (DApps)

![DApps](./01.png)

Why Decentralized Applications?

![Why DApps](./02.png)

Why Learn Ethereum

![Why Learn Ethereum](./03.png)

Ethereum Applications

![Ethereum Applications](./04.png)

Ethereum Platform

![Ethereum Platform](./05.png)

Course Plan

![Course Plan](./06.png)

Course Requisites

![Course Requisites](./07.png)

## 2.2 Blockchain Technology

History of Blockchain

![History of Blockchain](./08.png)

![History of Blockchain 2](./09.png)

Centralized Financial Institution

![CFI](./10.png)

Issues with Banking System

![Issues](./11.png)

Financial System with Bitcoin

![FSB](./12.png)

Bitcoin Cryptocurrency

![Bitcoin Crypto](./13.png)

Blockchain

![Blockchain](./14.png)

Blocks Generation

![Blocks Generation](./15.png)

![Blocks Generation](./16.png)

![Blocks Generation](./17.png)

![Blocks Generation](./18.png)

Operations on Blockchain

![Operations on Blockchain](./19.png)

## 2.2 Hash Functions

![Hash Functions](./20.png)

![Hash Functions 2](./21.png)

![Hash Functions 3](./22.png)

![Hash Functions 4](./23.png)

## 2.3 Ethereum Overview

Origins of Ethereum

![Origins](./24.png)

One Blockchain per Application

![One Blockchain per Application](./25.png)

The World Computer

![The World Computer](./26.png)

History of Ethereum

![History of Ethereum](./27.png)

Ethereum

![Ethereum](./28.png)

Ethereum in a nutshell

![Ethereum in a Nutshell](./29.png)

Ethereum Projects

![Ethereum Projects](./30.png)

Types of Ethereum Networks

![Types](./31.png)

## 2.4 Ethereum Wallets

![Ethereum Wallets](./32.png)

Ethereum Accounts

![Ethereum Accounts](./33.png)

Ethereum Wallet

The wallet reflects the transactions related with our account

![Ethereum Wallet](./34.png)

Signing Transactions

![Signing Transactions](./35.png)

Where to get Ether?

![Where to Get Ether](./36.png)

Test Networks

![Test Networks](./37.png)

![Test Networks 2](./38.png)

Faucets

![Faucets](./39.png)

## 2.5 Using Ethereum

Demo

![Demo](./40.png)

I have  used the metamask as Wallet.

Faucet used: faucet.rinkeby.io

Needed to sign-up in Twitter, write a post with my public address and then got 3 ETH finally.

![Metamask Rinkeby](./41.png)

![1 ETH from Cuenta 1 to Cuenta 2 - (view cuenta1)](./42.png)

![1 ETH from Cuenta 1 to Cuenta 2 - (view Cuenta2)](./43.png)

# 3. Getting started with Smart Contracts

## 3.1 Module Overview

![Module Overview](./44.png)

![Goals of this module](./45.png)

## 3.2 Smart Contracts

![Smart Contract](./46.png)

![Smart Contracts Languages](./47.png)

![Smart Contracts](./48.png)

![Smart Contracts Structure](./49.png)

![Types in Solidity](./50.png)

![Variables in Solidity](./51.png)

![Constants in Solidity](./52.png)

![Operators](./53.png)

![Comparision Operators](./54.png)

![Comments](./55.png)

![Return Values](./56.png)

## 3.3 Encapsulation in Solidity

![Encapsulation](./57.png)

external: only from exterior
public: can be called from outside or inside
none: equals as public
internal: can be called from inside not outside
private: can be called from inside not outside

The difference between internal and private is related to inheritance

![Encapsulation](./58.png)

![Field Modifiers](./59.png)

## 3.4 Smart Contracts Execution

![Creating Smart Contracts](./60.png)

![Ethereum Bytecode](./61.png)

![Smart Contract Compilation](./62.png)

![Ethereum Bytecode](./63.png)

![Ethereum Bytecode](./64.png)

![Stack Based VM](./65.png)

![Stack Based VM 2](./66.png)

## 3.5 Transactions in Ethereum

![Changing a Blockhain State](./67.png)

![Transactions and Ethereum State](./68.png)

![Transactions and Ethereum State 2](./69.png)

![Transaction Structure](./70.png)

nonce: transaction number for a particular account

__Creating a new contract__

![New Contract](./71.png)

![Propagate and validation](./72.png)

![Creates new block in a peer](./73.png)

![Propagates block and validation](./74.png)

![Bytecode prepared](./75.png)

__Calling a method__

![Call method](./76.png)

![Call method](./77.png)

![Call method](./78.png)

![Call method](./79.png)

__Block Fiels__

![Block Fields](./80.png)

__Contracts Limitation__

![Contracts Limitation](./81.png)

## 3.6 First Smart Contract

![First Smart Contract](./82.png)

We will use Remix as IDE online.

https://remix.ethereum.org/

![Remix IDE online](./83.jpg)

We delete the two examples and will create our Helloworld.sol

```solidity
pragma solidity ^0.4.0;

contract HelloWorld {
    string public message;
    
    function seetMessage(string newMessage) public {
        message = newMessage;
    }
}
```
Entering in Solidity Environment, check 0.4.25 versión of the compiler and compile it

![Compilation](./84.jpg)

Clicking on Compilation Details

![Compilation Details](./85.jpg)

We can run the program clicking on the icon "Run and deploy transactions"

![Run and deploy transactions](./86.jpg)

We choose:

- Environment: Javascript VM, Injected Web 3 or Web3 provider
- Account: different accounts to execute a transaction
- Gas limit: gas that are willing to pay executing deploying the smart contract
- Value: amount of ether we want to send with a transaction

Clicking on deploy

![Deployed](./87.jpg)

And we can test our contract

![Testing our contract](./88.jpg)

## 3.7 Paying for Computation

![Paying for Computation](./89.jpg)

![Gas](./90.jpg)

![Estimation Gast](./91.jpg)

![Gas and Refund](./92.jpg)

![Ethereum Node Types](./93.jpg)

![Ethereum Denominations](./94.jpg)

## 3.8 Transactions and Calls

![Transactions and calls](./95.jpg)

![Function modifiers](./96.jpg)

Se usa "pure" para indicar explicitamente que la función no modifica ningún estado

## 3.9 Removing Contracts

![Deploying Contract with Remix](./97.jpg)

![Removing Contracts](./98.jpg)

![Selfdestruct](./99.jpg)

![Using Metamask](./100.jpg)

Metamask uses Infura to access the Ethereum Network indirectly by default or could be access directly to a Ethereum node passing its address.

## 3.10 Deploying Smart Contracts

![Demo](./101.jpg)

We will create a new function called remove (is not secure, because all people could call it, we will view how to secure the calling of function methods)

```
pragma solidity ^0.4.0;

contract HelloWorld {
    string public message;
    
    function setMessage(string newMessage) public {
        message = newMessage;
    }
    
    function remove() public {
        selfdestruct(0x0);
    }
}
```

Compile it, and then select Injected Web3, specifing the environment as Injected Web3 (if we are using metamask, the remix will connet with it)

![Setting the environment](./102.jpg)

Our main account in metamaks must be shown by default, indicating our funds.

Now, we click on Deploy button to deploy the smart contract. Then will appear the next metamask popup

![Metamask popup](./103.jpg)

Click the "Confirm" button and then, the contract will be deployed

![Contract deployed shown in Remix](./104.jpg)

And in Metamask

![Contract pending shown in Metamask](./105.jpg)

We finally need to click the confirm on Metamask, and then we will obtain the smart contract deployed OK.

![Contract deployed shown in Metamask](./106.jpg)




