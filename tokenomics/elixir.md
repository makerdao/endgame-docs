# Elixir

Elixir is the long term liquidity solution for Dai, EtherDai and MKR. It is a liquidity pool token of one third DAI, one third liquid staked Ether tokens and one third MKR. Elixir will be used to provide sustainable liquidity on ethereum mainnet and all L2 networks. 

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

## Endgame Interactions

Maker Core accumulates Elixir using a share of its surplus capital. This Elixir will be used to burn MKR in bursts, when the MKR price is favourable.

SubDAOs also accumulate Elixir using their surplus capital. The relative amount of Elixir held by each SubDAO will determine their share of MKR emissions from Maker Core. The more Elixir a SubDAO holds, the more MKR emissions it will recieve.

SubDAOs burn a small percentage of their governance token each year if the value of their accumulated Elixir exceeds their token's market cap. This delivers value back to the SubDAO's token holders.

Responsibility for Elixir comes under the Protocol Engineering Scope.

## Elixir Development

In the first version, Elixir will be a simple Balancer pool that consists of one third Dai, one third Lido stETH and one third MKR. This initial implementation has no dependency on EtherDAI which speeds up deployment. Later, the Balancer pool will be modified to replace stETH with EtherDAI.

In its final form, Elixir will consist of one third Dai, one third EtherDai and one third MKR.

## Related Pages
{% content-ref url="etherdai.md" %} EtherDai {% endcontent-ref %}
{% content-ref url="subelixir.md" %} SubElixir {% endcontent-ref %}
{% content-ref url="subDAOs.md" %} SubDAOs {% endcontent-ref %}  

>Page last reviewed: -    
>Next review due: -   