# ETHPrague Hackathon 2023

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

## Introduction to API3 for ETHPrague Hackers

[API3](https://api3.org/) is a collaborative project that delivers oracle services to smart contracts in a decentralized and trust-minimized way. It is governed by a decentralized autonomous organization (DAO), namely the [API3 DAO](https://api3.org/dao).

- [API3 Docs](https://docs.api3.org/)
- [Github](https://github.com/api3dao/)
- [Medium](https://medium.com/@api3)

### API3's oracle stack

Airnode is a serverless function that lets API providers run their own oracle nodes. That way, they can provide data to any on-chain dApp that's interested in their services without an intermediary.

First-party oracles provide a more secure and reliable oracle, whilst enabling dApps to transparently understand the data source. 

ou can [learn more about first-party oracles](https://docs.api3.org/guides/airnode/calling-an-airnode/) or [dAPIs](https://docs.api3.org/explore/dapis/what-are-dapis.html) within the API3 Documentation. 

### API3 data feeds: dAPIs

dAPIs provide smart contracts with access to continuously updated feeds of market data. API3 data feeds can be accessed in two methods:

1- Self-funded dAPIs see users add collateral for oracle operatation and are permissionless. They provide an efficient and secure data feed source, with off-chain agreegation. 
2- Managed dAPIs are operated by the API3 DAO and requires authorization. They are powered by mutliple first-party oracles with native-chain agreegation, offering a decentralized oracle solution. 

Once a dAPI has been imported a smart contract can access a range of data feed services through the [API3 Market](https://market.api3.org/dapis). 

# Get started with dAPIs 

To get started all you have to do is import the `IProxy` Interface, and call the `read()` function. 

```solidity
pragma solidity 0.8.17;

import "@api3/contracts/v0.8/interfaces/IProxy.sol";

contract DataFeedReaderExample {
    ...

    function readDataFeed()
        external
        view
        returns (int224 value, uint256 timestamp)
    {
        // proxyAddress is the address of the proxy contract for
        // the dAPI you want to read.
        // Head over to https://market.api3.org to get the proxy
        // address for the dAPI you want. 
        (value, timestamp) = IProxy(proxyAddress).read();
    } 
}
``` 

<!-- Do we need to add a link to the above?-->

### Additional learning resources 

dAPIs give DeFi builders access to over 130 forex & crypto dAPIs that serve real-time market data to 10 networks (and 11 testnets). The below resources will help you get started with first-party data feeds.

Learn more: 

- [Activating a self-funded dAPI](https://docs.api3.org/guides/dapis/subscribing-self-funded-dapis/)
- [Reading a dAPI](https://docs.api3.org/guides/dapis/read-self-funded-dapi/)
- [API3 data feed reader example](https://github.com/api3dao/data-feed-reader-example)

Tutorials: 

- [Using dAPIs on zkSync Era Testnet](https://vanshwassan.medium.com/using-dapis-on-zksync-era-testnet-30f12efdd95f)
- [Making on-chain Payments and mint NFT Receipts using dAPIs](https://medium.com/@vanshwassan/making-an-on-chain-payment-and-minting-an-nft-receipt-with-permissionless-price-oracles-a7339f7b8c3e)
- [zkSync Paymasters with dAPIs](https://github.com/vanshwassan/zk-paymaster-dapi-poc)
- [EVM Paymasters with dAPIs]()

Or get started now with the API3 Market.

- [API3 Market](https://market.api3.org/)

# Hackathon Challenge: Using API3's First-party Oracles to power DeFi dApps

### 💸 Best DeFi Concept/Application: $2500 API3 Tokens

Use and correct integration of dAPIs within:

- Prediction market
- Lending application
- Perpetual swaps
- Derivative protocols 
- Decentralized insurance protocols
- Algorithmic stablecoin

Use of an API3 oracle within a zero-knowledge DeFi primitive will be considered within judging. 

### 🚀 Use of dAPIs in Paymasters: $1000 API3 Tokens

- dAPIs can be used within Paymaster contracts to enable users to pay for gas in any token of their choice on your platform.. You can follow the [Paymasters with dAPIs on zkSync](https://github.com/vanshwassan/zk-paymaster-dapi-poc) to support this submission.

### 🎰 Best use of API3 Oracle Stack: $500 API3 Tokens

- Using Airnode or API3 QRNG to facilitate a proper use-case. Participants are free to implement their own ideas.

### 😃 Best collaboratoor $1000 API3 Tokens

- When used with other technologies oracles can unlock exciting new use cases, we welcome builders using API3 with other stacks in the hackathon 

## Submission Requirements

All hackathon participants who are competing for the API3 bounties are required to submit a project that meets the following requirements:

- The project should be submitted to the ETHPrague Hackathon 2023 x API3 Devpost page by the deadline.
- Use of API3’s dAPIs/Airnode/QRNG that facilitates a proper use-case.
- The project should be live with a working frontend deployed.
- The project should be open-source with a public Github repository with the codebase, 
- The repo must be licenced with one of the following open source licences: GPL-3.0, or MIT.

## Judging criteria

Participants may submit a maximum of 1 project by the hackathon deadline. After submission, projects will be judged by the following criteria:

- **Real-world Functionality**: How well does the project work? Does it meet the minimum requirements?

- **Technical Difficulty**: How technically challenging was it to build the project?

- **Originality**: How original is the idea? How much does it differ from other existing solutions?

- **Design**: How well-designed is the project? Is it easy to use? Is it visually appealing?

- **BONUS** - Adding functionality to the Airnode protocol that will improve performance, interoperability, or further develop use cases.




<!--
![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)-->
