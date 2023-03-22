# SubDAOs

SubDAOs are semi-independent, specialized DAOs that are formed by MakerDAO and designed for protocol alignment. They allocate Dai collateral through decentralized frontends and handle the associated operational efficiency risk and marginal decision making.

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

## General Characteristics

SubDAOs have each their own unique governance token, governance processes, and workforce. They are driven by a self-determined, self-aware *meta* (understood as the non-quantifiable values, aspirations, and sensibilities within a human-operated organization &mdash; its ethos). They are, in most respects, self-standing, unique DAOs. Their semi-independent nature helps segregate complexity from Maker Core, alleviate the cognitive load of governance, and derisk MakerDAO by sandboxing the effects of subDAO operations. However, subDAOs governance processes run on top of MakerCore governance infrastructure and MKR holders hold control of their treasury.


## SubDAO Classes

SubDAOs are classified into three classes:

- **[Facilitator subDAOs](facilitator.md)**: Facilitate governance for other subDAOs, for scope frameworks, and for arbitration.
- **[Protector subDAOs](protector.md)**: Protect real-world collateral loans. They house RWA products and take on a first-loss position on all non-decentralized lending.
- **[Creator subDAOs](creator.md)**: Further decentralized collateral revenue streams. They focus on revenue and product generation.

## Easy Governance Frontends

Easy Governance Frontends (EGF) are the outward-facing presentation of subDAOs. They serve three functions:

1. Provide a place where subDAOs can express their brand and unique meta in order to connect with their community and funnel new users into using the protocol.
2. Provide access to the services provided by the subDAO (vanilla Maker Vaults plus any additional services the subDAO may offer &mdash; e.g., RWA vaults).
3. Provide governance tools for the subDAO and the broader MakerDAO.
    - These include Dai generation via MKR delegation (effectively MKR Vaults), and Dai staking for subDAO token rewards.

More details can be found in the [EGF page](../maker-core/easy-governance-frontend.md).

>Page last reviewed: 2023-03-22    
>Next review due: 2024-03-22    

