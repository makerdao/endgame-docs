# Collateral Breakdown

Collateral assets held by the Maker Protocol or its SubDAOs can be broken up into the following categories.

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## Decentralized collateral
1. Ether: Examples include Ether, Liquid Staking Derivatives such as stETH or rETH, ETH/DAI liquidity pool tokens or [EtherDAI](etherdai.md).
2. Miscellaneous: Examples include ERC-20 tokens such as UNI, LINK, etc. as well as liquidity pool tokens involving these assets.
3. MKR: Note that MKR no longer functions as the backstop used if DAI loses its peg.
4. SubDAO tokens: Note that the maximum exposure to subDAO tokens via [SubElixir](subelixir.md) is limited in Endgame. 

## RWA collateral
1. Cashlike: This refers to centralized stablecoins such as USDC and short term government bonds. Note that these are seizable.
2. Clean Money: This includes assets related to renewable energy projects, nuclear energy, sustainable agriculture, etc. Note that these are seizable.
3. Miscellaneous: All other real-world asset collateral including ERC-20 tokens such as WBTC, security tokens, and L1 bridge tokens. Note that these are seizable.
4. Physically Resilient: Theoretical but may be the only RWA collateral that are not legally seizable.

## Related Pages
{% content-ref url="etherdai.md" %} EtherDai {% endcontent-ref %}
{% content-ref url="subelixir.md" %} SubElixir {% endcontent-ref %}
{% content-ref url="subDAOs.md" %} SubDAOs {% endcontent-ref %}  

>Page last reviewed: 2023-01-20   
>Next review due: 2023-04-20    
