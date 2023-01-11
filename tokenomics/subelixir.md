# SubElixir

SubElixir is the core liquidity solution for SubDAO tokens. SubElixir is a set of liquidity pool tokens (one for each SubDAO) made up 50% MKR and 50% SubDAO token.

Each SubDAO has both a SubDAO token and a SubElixir LP token.

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

## Endgame Interactions

Maker Core emits MKR that it uses to the benefit of the SubDAO. The more Elixir a SubDAO holds, the more MKR emissions it will receive from Maker Core.

Maker Core will use MKR emissions in one of two ways, depending on whether the SubDAO token is undervalued or overvalued. If the SubDAO token is undervalued, Maker Core will accumulate SubElixir. If the SubDAO token is overvalued, Maker Core will accumulate Elixir and transfer it to the SubDAO. 

Maker Core benefits from the success of SubDAOs because it holds each SubDAOs SubElixir token. If a SubDAO's token is worth more, its SubElixir LP also becomes worth more. This causes its SubElixir liquidity pool to rebalance in favour of MKR, adding demand for the MKR token to the market and benefiting Maker Core.

## SubElixir Development

Maker will create the SubElixir tokens for the initial SubDAOs as a simple Uniswap V2 pool token. 

## Related Pages
{% content-ref url="etherdai.md" %} EtherDai {% endcontent-ref %}
{% content-ref url="elixir.md" %} Elixir {% endcontent-ref %}
{% content-ref url="SubDAOs.md" %} SubDAOs {% endcontent-ref %}  

>Page last reviewed: 2023-01-11    
>Next review due: 2023-04-11   