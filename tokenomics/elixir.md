# Elixir

{% hint style="info" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented.
{% endhint %}

Elixir is the long term liquidity solution for Dai, EtherDai and MKR. It is a liquidity pool token of one third DAI, one third liquid staked Ether derivatives and one third MKR. Elixir will be used to provide sustainable liquidity on ethereum mainnet and all L2 networks. 

{% hint style="warning" %}
The Endgame plan is currently in a dynamic and evolving state. Be aware that parts of this documentation may be out of date or incorrect.
{% endhint %}

## Interactions

Maker Core accumulates Elixir using a share of its surplus capital. This Elixir will be used to burn MKR in bursts, when the MKR price is favourable.

SubDAOs also accumulate Elixir using their surplus capital. The relative amount of Elixir held by each subDAO will determine their share of MKR emissions from Maker Core. The more Elixir a MetaDAO holds, the more MKR MakerCore will use to buy SubElixir.

SubDAOs burn a small percentage of their governance token each year if their accumulated Elixir exceeds their token's market cap. This delivers value back to the subDAOs token holders.

Responsibility for Elixir comes under the Protocol Engineering Scope.

## Elixir Development

In the first version, Elixir will be a simple Balancer pool that consists of one third Dai, one third stETH and one third MKR. This initial implementation has no dependency on EtherDAI which speeds up deployment. Later, the Balancer pool will be modified to replace stETH with EtherDAI.

In its final form, Elixir will consist of one third Dai, one third EtherDai and one third MKR.

## Related Pages
{% content-ref url="etherdai.md" %} EtherDai {% endcontent-ref %}  
{% content-ref url="subelixir.md" %} SubElixir {% endcontent-ref %}  
{% content-ref url="..\subDAOs\subDAOs.md" %} SubDAOs {% endcontent-ref %}  

>Page last reviewed: 2023-01-09    
>Next review due: 2023-04-09    