# Protector SubDAOs

Protector subDAOs focus on intermediating Maker Core's interaction with the physical, regulated, law-bound real world. Concretely, their primary focus is to facilitate and implement real-world asset collateralization. They are also tasked with protecting its RWA collateral against legal and physical threats.

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

## RWA Vault Adoption

Protector subDAOs can only adopt vaults that conform either to the cashlike RWA collateral standard or to the Clean Money RWA collateral standard. 

RWA vault adoption must be ratified by Maker Governance through a vault adoption MIP, which sets the vault's debt ceiling and its capital cost &mdash;i.e., the minimum expected return&mdash;, which in turn defines how much of the Stability Fee for the adopted vault must go to Maker Core.

Protector subDAOs can use their internal governance processes to allocate up to its vault adoption Debt Ceiling to its arrangers.

Adopted vaults impose a first-loss position for the adopting protector subDAO on all downsides.

>Page last reviewed: 2023-03-30    
>Next review due: 2024-06-30    
