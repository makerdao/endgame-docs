# Easy Governance Frontend

{% hint style="warning" %}
This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date.
{% endhint %}

Easy Governance Frontends (EGFs) are standardized and regulated web applications for MKR delegation.

## Usability Goals

The primary goal of EGFs is to provide a standardized and unbiased platform used for delegation. This will include:
* Viewing [delegates](delegates.md) and their profiles.
* Viewing [constitutional voter committee](avc.md) profile pages and members.
* Viewing voting strategies.
* Representing the interactions between the above.

A key goal is that MKR Holders lacking context and interest in Maker Governance can still engage effectively.

At the start of early-game, [SubDAO tokens](../tokenomics/subdao-tokenomics.md) will be farmable with delegated MKR.

## Technical Goals

EGFs have a serverless design. Users can download them for local use without dependencies on hosting infrastructure.

EGFs will access required data in a decentralized way using the IPFS protocol. The root content ID hash will be recorded on-chain (likely on ENS) and data will be accessed by the client using IPFS.

At the start of early-game, SubDAOs will each host separate but identical EGF apps to improve accessibility.

>Page last reviewed: 2023-08-03      
>Next review due: 2023-11-03    
