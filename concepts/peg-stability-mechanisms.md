# Peg Stability Mechanisms

## Introduction

The Endgame Plan allows the Maker Protocol to dynamically impact the supply and demand of DAI. These mechanisms are called Peg Stability Mechanisms. Note that should not be confused with the similarly-named [Peg Stability Modules (PSMs)](https://manual.makerdao.com/module-index/module-psm)

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## DAI Savings Rate (DSR)

The [DAI Savings Rate](https://manual.makerdao.com/parameter-index/core/param-dai-savings-rate) already exists in Maker and remains unchanged in Endgame. It allows DAI holders to deposit DAI into the DSR contract and earn interest. The interest is paid from the protocol's profits. 

By changing the interest rate, Maker Governance can increase or decrease the circulating supply of DAI, which in turn influences the price of DAI on the open market.

## Stability Fee Base Rate (SBFR)

The Stability Fee Base Rate increases the stability fee of some or all vaults, increasing income to help fund the DSR. A related and similar parameter that already exists in Maker is the [Global Stability Fee](https://manual.makerdao.com/parameter-index/vault-risk/param-stability-fee#considerations) parameter.

By changing the stability fee base rate, Maker Governance can make it more or less profitable to mint DAI using vaults. This increases or decreases the circulating supply of DAI, which in turn influences the price of DAI on the open market.

## Target Rate (TR)

Certain [Stances](stances.md) in the Endgame Plan allow DAI to depeg from the US Dollar. The Target Rate determines the rate at which the Target Price of DAI changes over time. 

A positive TR increases demand for DAI and reduces the supply of DAI while a negative TR has the opposite effect. 

## Protocol-Owned Vault

The Protocol-Owned Vault is a special Maker Vault only usable by Maker Governance. It holds [EtherDAI](../tokenomics/etherdai.md) and potentially other decentralized assets as collateral. DAI can be minted by this vault. Note that this vault cannot be liquidated and has no Stability Fee.

Maker Governance may then purchase more EtherDAI with DAI minted from the Protocol-Owned Vault. This puts the protocol in a leveraged long position on EtherDAI and increases the supply of DAI. This action also increases the share of DAI backed by decentralized collateral and takes advantage of a potential negative TR. 


>Page last reviewed: 2023-01-31    
>Next review due: 2023-04-31  
