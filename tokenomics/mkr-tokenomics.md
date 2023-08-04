# MKR Tokenomics

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

MKR (Maker) is the preexisting governance token for the Maker Protocol. Under the Endgame Plan MKR is emitted and burned in various circumstances. 

## Stated Goals

There are multiple goals that Maker intends to meet via the new MKR tokenomics.

1. To successfully incubate Maker SubDAOs.
2. To link the value and success of Maker Core with that of its SubDAOs and vice versa.
3. To incentivize talented individuals to work as part of Maker Core.

## MKR Utility

SubDAO tokens will be farmable using MKR locked up in the [Sagittarius Engine](sagittarius-engine.md).

## MKR Emissions

Maker Core emits a total of 60,000 MKR each year which is allocated to benefit its subDAOs. Depending on whether each SubDAO token is undervalued or overvalued, MKR emissions are used in one of two ways:
* If a SubDAO token is undervalued, Maker Core accumulates [SubElixir](subelixir.md). 
* If a SubDAO token is overvalued, Maker Core accumulates [Elixir](elixir.md) and transfers it to the SubDAO. 

Each path results in the emitted MKR entering a liquidity pool. In the first case, MKR is paired with SubDAO tokens, and in the second case, MKR is paired with Dai.

Maker Core also emits a total of 5,000 MKR each year which it uses to:
* Incubate new SubDAOs
* Provide decentralized workforce bonuses.

Additionally, Maker Governance may now opt to interrupt the automatic use of MKR as a backstop for Dai value in the event of bad debt in the Maker Protocol. Instead, Maker Governance may choose to modify Dai's Target Price, resulting in a loss of value for all Dai holders.

## MKR Burns

The Endgame plan introduces the Maker Smart Burn Engine. The Smart Burn Engine accumulates Elixir using Maker Core protocol surplus. This accumulation of Elixir benefits Dai and MKR liquidity. The Reverse Burn Engine uses its accumulated Elixir to buy and burn MKR when MKR is judged to be undervalued according to a valuation model.

## Launch Overview

![Maker Core Tokenomics](../assets/images/core-tokenomics.png)

>Page last reviewed: 2023-08-03    
>Next review due: 2023-11-03   