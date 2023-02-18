# Sagittarius Engine

## Introduction
The Sagittarius Engine adds new two new utilities to the MKR token. MKR can be used to 
- Farm SubDAO tokens
- Generate Dai using MKR as collateral

{% hint style="warning" %} This documentation describes planned functionality and processes that MakerDAO has not yet implemented. Be aware that parts may be inaccurate or out of date. {% endhint %}

## Usage
Users may deposit MKR into the Sagittarius Engine. When depositing, they automatically delegate the deposited MKR through the Protocol Delegation System (PDS). Depositors must specify a target delegate smart contract through the PDS when making their deposit.

## Farming
When users make their deposit, they can choose one of several ERC-20 tokens to farm. This functionality will initially be disabled with no available tokens to farm. 

Maker Governance can later add farmable SubDAO governance tokens, making the first version of the Sagittarius Engine compatible with the launch of SubDAOs.

Token farming automatically ends when the user wishes to withdraw their MKR from the Sagittarius Engine.

## MKR Vaults
The Sagittarius Engine allows users to use deposited MKR as collateral to generate Dai, similar to normal Maker Vaults. 

The oracle for MKR prices used to manage these MKR vaults has constrained upwards movement. That is, Maker Governance can choose to limit the speed at which the reported price of MKR increases, regardless of how fast the price is actually increasing. This constraint does not apply to downward price movement. 

When an MKR vault is liquidated, the MKR is automatically undelegated and put up for auction. Token farming also automatically stops when a vault is liquidated.


>Page last reviewed: 2023-02-13    
>Next review due: 2023-05-13  






