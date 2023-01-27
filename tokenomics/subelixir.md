# SubElixir

SubElixir is the core liquidity solution for SubDAO tokens. SubElixir is a set of liquidity pool tokens (one for each SubDAO) made up 50% MKR and 50% SubDAO token.

Each SubDAO has both a SubDAO token and a SubElixir token.

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

## Endgame Interactions

Maker Core emits a fixed amount of MKR that it uses to the benefit of the SubDAOs. These MKR emissions are split between SubDAOs. The more [Elixir](elixir.md) a SubDAO locks, the larger the share of MKR emissions it receives from Maker Core. However, there is an upper limit on the share of the emissions that any single subDAO can claim.

Maker Core uses MKR emissions in one of two ways, depending on whether the SubDAO token is undervalued or overvalued. If the SubDAO token is undervalued, Maker Core accumulates SubElixir. If the SubDAO token is overvalued, Maker Core accumulates Elixir, locks it, and tranfers it to the SubDAO. 

Maker Core benefits from the success of SubDAOs because it holds each SubDAOs SubElixir token. If a SubDAO's token is worth more, its SubElixir LP also becomes worth more. This causes its SubElixir liquidity pool to rebalance in favour of MKR, adding demand for the MKR token to the market and benefiting Maker Core.

## SubElixir Development

Maker will create the SubElixir tokens for the initial SubDAOs as Uniswap V2 liquidity pool tokens. 

>Page last reviewed: -    
>Next review due: -   