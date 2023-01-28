# Collateral Breakdown

Collateral assets held by the Maker Protocol or its SubDAOs can be broken up into the following categories.

## Decentralized 
1. **Ether:** Examples include Ether, Liquid Staking Derivatives such as stETH or rETH, ETH/DAI liquidity pool tokens or [EtherDAI](../tokenomics/etherdai.md). These are assets that are guaranteed to be truly decentralized and resilient at scale. The Endgame plan incentivizes increasing ETH-based collateral through the SubDAO yield farming for EtherDAI, and uses the Protocol-Owned Vault to accumulate more EtherDAI over time.

2. **Miscellaneous decentralized:** Examples include ERC-20 tokens such as UNI, LINK, etc. as well as liquidity pool tokens involving these assets. These make DAI as decentralized and unbiased as possible. However, they are rarely scalable enough to be useful as collateral directly in Maker Core. Such tokens are mostly the responsibility of SubDAOs.

3. **MKR:** The Endgame Plan significantly changes the tokenomics of MKR. The solvency backstop is no longer enforced and instead becomes optional. MKR can then be used as decentralized collateral to generate DAI through overcollateralized vaults. MKR can generate stability fees for the protocol, participate in governance, and farm SubDAO tokens. 

4. SubDAO tokens: These tokens are a source of decentralized collateral that can be used in overcollateralized vaults to generate DAI. However, SubDAO tokens also provide a solvency backstop to the SubDAOs. As a result, the maximum exposure to subDAO tokens via [SubElixir](../tokenomics/subelixir.md) is limited in Endgame. 

## Real-World Assets (RWA) 
1. **Cashlike:** This refers to centralized stablecoins such as USDC and short-term government bonds. The role of these assets is to provide liquidity for DAI and enable its use as a currency. The major downside with Cashlike RWA is that they can be seized easily.

2. **Clean Money:** This includes assets related to renewable energy projects, nuclear energy, sustainable agriculture, etc. Note that these are also seizable but provide Maker with strong meta due since the projects they fund benefit the public.

3. **Miscellaneous:** All other real-world asset collateral including ERC-20 tokens such as WBTC, security tokens, and L1 bridge tokens. Note that these are seizable, even when they are ERC-20 tokens.

4. **Physically Resilient:** The Endgame Plan assumes that at a point in the future, there will be a severe crackdown on use of RWA in crypto. Anything that can be seized by global powers may be at risk of seizure through legal means. Physically Resilient RWA are real-world assets that cannot easily be seized. A DAO like Maker can retain some level of technical sovereignty over such assets. 

>Page last reviewed: 2023-01-27   
>Next review due: 2023-04-27   