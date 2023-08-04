# Elixir

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

Elixir is the long term liquidity solution for Dai and MKR. It is a liquidity pool token made up of 50% Dai and 50% MKR. Elixir is intended to ensure sustainable liquidity for MKR and Dai.

## Endgame Interactions

Maker Core accumulates Elixir using a share of its surplus capital. This Elixir is used to burn MKR in bursts, when the MKR price is favourable.

SubDAOs also accumulate Elixir using their surplus capital. SubDAOs may lock their Elixir. The relative amount of Elixir locked by each SubDAO determines their share of MKR emissions from Maker Core. The more locked Elixir a SubDAO holds, the more MKR emissions it recieves.

SubDAOs use locked Elixir to burn a small percentage of their governance token each year if the value of their locked Elixir exceeds their token's market cap. This transfers value back to the SubDAO's token holders.

## Elixir Development

In the first version, Elixir will be Uniswap V2 DAI/MKR liquidity pool tokens.

>Page last reviewed: 2023-08-03    
>Next review due: 2023-11-03   