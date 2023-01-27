# Stances

## Introduction

The Endgame Plan requires the Maker Protocol to handle significant changes in regulatory frameworks and macroeconomic circumstances. The protocol can adopt three possible stances to balance risk and long-term reward as it reacts to these changes. 

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## Operational aspects

The switch to a new stance is triggered by certain predetermined conditions that are part of the Endgame Plan approval. 

Each Stance also has automatic targeting rules for the Dai Savings Rate, the Stability Fee Base Rate, the [Target Rate](concepts/peg-stability-mechanisms.md) that determines the Target Price of DAI, and restrictions on the types of assets that may be held as collateral.

## Pigeon Stance 

Pigeon Stance is the intial stance at the launch of Endgame. It is assumed that the regulatory threat is still minimal and global economic conditions are stable. Under this stance
- DAI remains pegged to 1 USD.
- Income from RWA collateral is encouraged to build up protocol-owned surplus.

Pigeon Stance is expected to last for 2.5 years from the launch of the Endgame Plan. The protocol then automatically switches to Eagle Stance. Depending on regulatory and risk analyses, the length of the Pigeon Stance may be reduced or extended.

## Eagle Stance

Under Eagle Stance, two main changes occur:
- Maker’s exposure to seizable RWA is limited to a percentage of total collateral.
- DAI is no longer necessarily pegged to 1 USD. 

DAI is allowed to depeg from the USD using a negative Target Rate. This ensures that DAI is immune to possible regulatory crackdown that seizes RWA collateral. 

Eagle Stance has a six-month windup period where there are limits on how negative the Target Rate can be. This limit is removed after 6 months. There is no current expectation on how long the protocol may stay in Eagle Stance.

## Phoenix Stance

Phoenix Stance is Maker's most resilient stance. It is only triggered if there are clear signs of an impending attack on the RWA collateral, or if there is general global economic and geopolitical instability. 

The main changes to the protocol under this stance are:
- No easily seizable RWA collateral is allowed.
- The Target Rate and Target Price of DAI are determined without reference to [Peg Stability Mechanisms](concepts/peg-stability-mechanisms.md) or prices of other currencies respectively.

>Page last reviewed: 2023-01-27    
>Next review due: 2023-04-27  
