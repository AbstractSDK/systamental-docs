---
title: Vaults Overview
sidebar_position: 0
slug: /vaults-overview
keywords: [tokenized vaults, abstract vaults]
---



# Abstract Vaults {#1d746a0cd0c380e49ae4c84f74b8384d}


## What Are Abstract Vaults? {#1d746a0cd0c3808389d8d68717e70991}


### Tokenized Vaults {#1d746a0cd0c3803c92b4d0ef54efd5b2}


A **tokenized vault** is an **on-chain** investment pool that issues digital tokens representing an investor’s share of the underlying assets.

- **Mechanics**: Investors deposit assets (like stablecoins or crypto), and the vault’s smart contract automatically deploys those funds according to a predefined strategy.
- **Vault Tokens**: These tokens are **ERC-20** assets on Ethereum or other blockchains, meaning they can be transferred or traded globally, 24/7.
- **Real-Time Transparency**: Anyone can verify the vault’s contents, performance, and transactions on the blockchain—reducing reconciliation errors and increasing trust.

**Read more:** [Tokenized Funds - TradFi vs Onchain Vaults](/tokenized-funds)


### Abstract Vaults {#1d746a0cd0c3801ea36ac5405d161add}


Abstract Vaults extend this concept by enabling:

- **Multiple strategies** per-vault, allowing for maximum returns
- Exposure to **leveraged perpetuals** and **yield-bearing spot assets** across multiple exchanges and chains
- Integration of **intent-based execution** for access to deep liquidity (e.g., Binance-level order flow)
- Yield-enhancing strategies like **portable alpha** and **return optimization**

Our vaults are fully [ERC-4626](http://ethereum.org/en/developers/docs/standards/tokens/erc-4626)-compatible and support the [ERC-7540](https://eips.ethereum.org/EIPS/eip-7540) extension for asynchronicity. Read more in our protocol documentation here (coming soon).


## Why Vaults Matter {#1d746a0cd0c380adaed1dc31fd52d24c}


Vaults are the foundation of modern digital asset management. Abstract Vaults offer a modular approach to constructing high-performance portfolios, removing the need for users to manage positions or bridge assets manually. We put tools typically reserved for hedge funds directly into your hands.


They enable:

- **Multi-asset exposure** (e.g. BTC, ETH, Gold, stables)
- **Automated position rebalancing**
- **Up to 50x leverage** on supported assets
- **Return stacking** (combine yield + exposure)
- **Composable vault tokens** usable across DeFi
- **Asynchronous execution** for scalable capital deployment

## How Abstract Vaults Work {#1d746a0cd0c380d2bf8cdfc061448f5d}


Abstract Vaults operate asynchronously, similar to closed-end mutual funds. Vaults accept deposits and process redemptions on scheduled rebalance windows, configurable by the strategist, but often daily.


### **Deposits & Share Minting** {#1d746a0cd0c380038f3ef4644251139e}

1. Users deposit supported assets and receive a `depositId`
2. Shares are **minted at the next rebalance window** based on the vault’s Net Asset Value (NAV)
3. All users depositing within the same period receive **identical share prices**

### **NAV Calculation** {#1d746a0cd0c38016a5b9eb77cd7cc272}

1. Vault NAV is calculated by aggregating the value of positions across all chains
2. NAV reflects both spot and perp holdings, including offchain or DeFi positions
3. NAV is finalized once per rebalance window (e.g. daily)

### **Rebalancing** {#1d746a0cd0c380498f8cf875bc8661c0}

1. Strategy inputs (from quant models, offchain signals, or vault managers) drive allocation changes
2. Rebalances move capital between chains, perps, and yield strategies via:
	- Intent-based execution (for high liquidity needs)
	- Cross-chain messaging (for protocol-level state changes)
3. All rebalancing is **batched and non-interactive**

### **Withdrawals & Redemptions** {#1d746a0cd0c3800899c0c0297fe34df8}

1. Users requests a withdrawal by submitting their vault shares, tracked by a `withdrawalId`
2. Withdrawals are processed at the **next rebalance window**, based on the current NAV
3. Users receive underlying assets or bridged equivalents.

## Token Liquidity & Trading {#1d746a0cd0c3802680d6f9a07b9f8caa}


Vault shares are fully composable ERC-20 tokens.

- Can be LP’d on DEXes for **instant liquidity**
	- LPing introduces **impermanent loss risks**, but also enables arbitrage between NAV and market price
- Vaults can be integrated into protocols like [**Morpho**](https://morpho.org/), [**Pendle**](https://pendle.finance/), or used as collateral within Abstract (coming soon)

## Risk Management {#1d746a0cd0c3809daeb1c9846e797295}


Abstract Vaults are designed with multiple layers of risk mitigation:

- **Oracles:** Secure price feeds for accurate NAV and leverage control
- **Asynchronous execution:** Limits slippage and protects from MEV
- **Vault-level controls:** Strategist-defined caps, slippage limits, and allocation constraints
- **Daily monitoring:** Vaults are monitored for strategy drift and execution integrity

## Fees {#1d746a0cd0c380529e51cd98595d661f}


Vault strategists may set their own fee structure, including:

- **Performance fees**
- **Management fees**
- **Execution fees (e.g. rebalance costs)**

Fees are defined by the vault strategist and disclosed in vault metadata. Fee changes must pass through a defined timelock contract to dissuade manipulation.


## Example Strategies {#1d746a0cd0c38019bd11cb790c345156}


Each strategy links to a detailed doc page.

- [TrendBTC](/trend-btc) Vault
- **BitGold Vault** (Coming Soon)

## Integrating Abstract Vaults {#1d746a0cd0c3801c8f7fc4a7bd9bb4a4}


Vaults can be surfaced in any frontend, wallet, or protocol UI. SDKs, APIs, and vault registry metadata available for integrators can be found in our protocol documentation (coming soon).


:::caution

**Note:** Vaults operate asynchronously. Integrations **must account for**:
- `depositId`based share minting

- Daily (or periodic) redemption windows

- Optional LP wrappers for continuous liquidity

:::



