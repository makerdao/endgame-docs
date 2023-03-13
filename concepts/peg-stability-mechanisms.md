# Peg Stability Mechanisms

## Introduction

The Endgame Plan introduces new mechanisms to complement existing mechanisms in the Maker Protocol to dynamically impact the supply and demand of Dai. These mechanisms are called Peg Stability Mechanisms. Note that this term should not be confused with the similarly-named [Peg Stability Modules (PSMs)](https://manual.makerdao.com/module-index/module-psm).

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## Dai Savings Rate (DSR)

The [Dai Savings Rate](https://manual.makerdao.com/parameter-index/core/param-dai-savings-rate) already exists in Maker and remains unchanged in Endgame. It allows Dai holders to deposit Dai into the DSR contract and earn yield at a rate known as the DSR. The yield is paid from the protocol's system surplus. 

By changing the DSR rate, Maker Governance can increase or decrease the circulating supply of Dai, which in turn influences the price of Dai on the open market.

## Stability Fee Base Rate (SFBR)

The Stability Fee Base Rate increases the stability fee of some or all vaults, increasing income to help fund the DSR. A related and similar parameter that already exists in Maker is the [Global Stability Fee](https://manual.makerdao.com/parameter-index/vault-risk/param-stability-fee#considerations) parameter.

By changing the Stability Fee Base Rate, Maker Governance can make it more or less expensive to mint Dai using vaults. This increases or decreases the circulating supply of Dai, which in turn influences the price of Dai on the open market.

## Target Rate (TR)

Certain [Stances](stances.md) in the Endgame Plan allow Dai to depeg from the US Dollar. The Target Rate determines the rate at which the Target Price of Dai changes over time. 

A positive TR increases demand for Dai and reduces the supply of Dai while a negative TR has the opposite effect.

For example, a TR of -5% implies that the protocol aims to decrease the Target Price of Dai at the rate of 5% per year. 

The TR is an extremely powerful tool as it accomplishes several goals, especially when it is negative.
 - It enables Maker to withstand a regulatory crackdown that seizes RWA collateral. The target rate may become more negative to reflect a higher risk of RWA collateral being seized.
 - It encourages Dai generation by ordinary users from decentralized collateral such as EtherDai. This is because of the expectation that Dai price will be lower when repaying the loan than it was when the vault was opened. 

Despite these benefits, the cost of breaking from the USD peg is also very high. Once the peg has been broken, the expectation that 1 Dai is always worth 1 USD can never be regained.

## Protocol-Owned Vault

The Protocol-Owned Vault is a special Maker Vault only usable by Maker Governance. It holds [EtherDai](../tokenomics/etherdai.md) and potentially other decentralized assets as collateral. Governance can mint Dai against the collateral held in this vault. Note that this vault cannot be automatically liquidated and has no Stability Fee.

Maker Governance may then purchase more EtherDai with Dai minted from the Protocol-Owned Vault. This puts the protocol in a leveraged long position on EtherDai and slightly increases the supply of Dai. This action also slightly increases the share of Dai backed by decentralized collateral. 

Finally, a leveraged long position using the Protocol-Owned Vault is synergistic with a negative Target Rate. This is because debt denominated in Dai becomes cheaper to repay as the Target Price of Dai decreases.


>Page last reviewed: 2023-02-03    
>Next review due: 2023-05-03  
