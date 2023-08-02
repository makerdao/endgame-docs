# Sagittarius Engine

## Introduction
The Sagittarius Engine is a module that incentivizes MKR holders to lock their MKR tokens up for long periods of time. The locked-up MKR is required to participate in Maker Governance via delegation. 

The incentives for locking up MKR in the Sagittarius Engine are:
- Token farming
- Dai generation through vaults with MKR as collateral

Withdrawing MKR from the Sagittarius Engine burns part of the deposited MKR.

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## Entry and Exit
When users deposit MKR into the Sagittarius Engine, they must delegate the deposited MKR through an [Easy Governance Frontend (EGF)](../maker-core/easy-governance-frontend.md). Depositors must specify a delegate's strategy smart contract when making their deposit.

When a user withdraws their MKR from the Sagittarius Engine, 15% of the deposited MKR is burned.

## MKR Vaults
The Sagittarius Engine allows users to use deposited MKR as collateral to generate Dai, similar to normal Maker Vaults. The parameters for these vaults are below:

#### [Debt Ceiling](https://manual.makerdao.com/parameter-index/vault-risk/param-debt-ceiling) 
There is no hard Debt Ceiling for these MKR vaults. However, a [Debt Ceiling Instant Access Module](https://manual.makerdao.com/module-index/module-dciam) will be configured to ensure that the Debt Ceiling does not increase too fast. A Soft Debt Ceiling parameter is set based on the value of all protocol-owned and SubDAO-owned assets.

#### [Stability Fee](https://manual.makerdao.com/parameter-index/vault-risk/param-stability-fee) 
If the total Sagittarius Engine debt is less than the Soft Debt Ceiling, this is set to be equal to the [Dai Savings Rate](https://manual.makerdao.com/parameter-index/core/param-dai-savings-rate). It increases exponentially with the amount of Sagittarius Engine debt that exceeds the Soft Debt Ceiling.

#### Price Oracle
The oracle for MKR price uses [Elixir](elixir.md) as the primary data source. 

A "sticky price" feature can be activated to limit the upward movement of the price within a fixed time period. That is, Maker Governance can choose to limit the speed at which the reported price of MKR increases, regardless of how fast the Elixir price is increasing. This constraint does not apply to downward price movement. 

#### [Liquidation Ratio](https://manual.makerdao.com/parameter-index/vault-risk/param-liquidation-ratio)
The Liquidation Ratio is set to 200%. If a vault falls below this collateralization ratio, it is liquidated completely using Elixir order books.

Sagittarius Engine MKR Vaults also have an additional parameter called the Soft Liquidation Ratio, which is set to 300%. If a vault's collateralization ratio stays below this for a continuous 7-day period, it is liquidated. Vaults cannot be opened with a collateralization ratio less than the Soft Liquidation Ratio. 

When an MKR vault is liquidated, the MKR is undelegated and put up for auction. 

## Token Farming
When users make their Sagittarius Engine MKR deposit, they can choose one of several ERC-20 tokens to farm. Token farming ends when the user withdraws their MKR from the Sagittarius Engine or if their MKR vault is liquidated.

This functionality will initially allow MKR depositors to only farm Dai. 25% of the protocol surplus will be allocated to Sagittarius Engine Dai farmers. 

Maker Governance can later add farmable SubDAO governance tokens, making the first version of the Sagittarius Engine compatible with the launch of SubDAOs.

>Page last reviewed: 2023-07-21    
>Next review due: 2023-10-21







