# ETHPrague Hackathon 2023 x API3: Hackathon Instructions

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

## Introduction to API3 for ETHPrague Hackers

### Understanding API3

[API3](https://api3.org/) is a collaborative project that delivers traditional API services to smart contract platforms in a decentralized and trust-minimized way. It is governed by a decentralized autonomous organization (DAO), namely the [API3 DAO](https://api3.org/dao).

- [API3 Docs](https://docs.api3.org/)
- [Github](https://github.com/api3dao/)
- [Medium](https://medium.com/@api3)

Airnode is a first-party oracle that pushes off-chain API data to an on-chain contract. Airnode is a serverless function that lets API providers easily run their own oracle nodes. That way, they can provide data to any on-chain dApp that's interested in their services without an intermediary.

- [Learn more about first-party oracles](https://docs.api3.org/guides/airnode/calling-an-airnode/)

### dAPIs: first-party data feeds 

To get started with self-funded dAPIs, all you have to do is import the `IProxy` Interface, and call the `read()` function. 

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

API3 uses first-party oracles to power [dAPIs](https://docs.api3.org/explore/dapis/what-are-dapis.html). dAPIs are secure, transparent, and cost-efficient data feeds that connect smart contracts directly to first-party data sources.

Self-funded dAPIs give DeFi builders access to over **100 forex & crypto dAPIs that serve real-time market data** to 10 networks (and 11 testnets). 

- [Activating a self-funded dAPI](https://docs.api3.org/guides/dapis/subscribing-self-funded-dapis/)
- [Reading a dAPI](https://docs.api3.org/guides/dapis/read-self-funded-dapi/)
- [API3 data feed reader example](https://github.com/api3dao/data-feed-reader-example)
- [Using dAPIs on zkSync Era Testnet](https://vanshwassan.medium.com/using-dapis-on-zksync-era-testnet-30f12efdd95f)
- [Making on-chain Payments and mint NFT Receipts using dAPIs](https://medium.com/@vanshwassan/making-an-on-chain-payment-and-minting-an-nft-receipt-with-permissionless-price-oracles-a7339f7b8c3e)
- [zkSync Paymasters with dAPIs](https://github.com/vanshwassan/zk-paymaster-dapi-poc)
- [Paymasters with dAPIs]()

Or get started now with the API3 Market.

- [API3 Market](https://market.api3.org/)

# Hackathon Challenge: Using API3's First-party Oracles to power DeFi dApps

## Best DeFi Innovation Project: $3000 USDC

Builders can use API3's first-party oracles and datafeeds to build and serve decentralized financial servies like:

- Prediction market
- Lending application
- Perpetual swaps
- Derivative protocols 
- Decentralized insurance protocols
- Algorithmic stablecoin

## Best Non-DeFi Project: $500 USDC

- Using Airnode or QRNG to facilitate a proper use-case. Participants are free to implement their own ideas.

## Project that uses Paymasters with dAPIs within their projects: $1500 USDC

- Using Paymaster with dAPIs within the project to enable users to pay for gas in any token of their choice on your platform.

## Best content around API3: $500 API3 Tokens

- Blog posts and articles
- Videos and explainers
- Technical Tutorials
- Technical Documentation

## Best Airnode Protocol Improvement: $500 USDC

- Developer tooling around Airnode, dAPIs and other API3 products.
- Best Airnode use-case 

## Judging criteria

Participants may submit a maximum of 1 project by the hackathon deadline. After submission, projects will be judged by the following criteria:

- **Real-world Functionality**: How well does the project work? Does it meet the minimum requirements?

- **Technical Difficulty**: How technically challenging was it to build the project?

- **Originality**: How original is the idea? How much does it differ from other existing solutions?

- **Design**: How well-designed is the project? Is it easy to use? Is it visually appealing?

- **BONUS** - Adding functionality to the Airnode protocol that will improve performance, interoperability, or further develop use cases.

## Submission Requirements

All hackathon participants who are competing for the API3 bounties are required to submit a project that meets the following requirements:

- The project should be submitted to the ETHPrague Hackathon 2023 x API3 Devpost page by the deadline.
- Use of API3’s dAPIs/Airnode/QRNG that facilitates a proper use-case.
- The project should be live with a working frontend deployed.
- The project should be open-source with a public Github repository with the codebase, 
- The repo must be licenced with one of the following open source licences: GPL-3.0, or MIT.

## Prizes

|       Position       |     Prize    |
|----------------------|--------------|
|    |    |
|      |     |
|     |     |

<!--
![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)-->
