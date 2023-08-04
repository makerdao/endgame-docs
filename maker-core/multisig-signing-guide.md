# How to "Sign" a Message Using a Gnosis Safe Multisig

{% hint style="warning" %} 

**Signing messages from a multisig using the method in this guide requires submitting an on chain transaction and payment of gas fees.**

**MakerDAO and GovAlpha will not take responsibility for any negative outcome experienced by people that are following this guide.** 

**You are responsible for your own funds.**

**If you are uncomfortable or unsure of how to proceed, stop what you are doing and ask for help.** {% endhint %}

The Constitution and Arbitration Scopes require signed messages from both CVC Members and Constitutional Delegates in order to become "recognized". Signed messages are also required for other actions such as CVC Decisions. Currently, there is no easy-to-use method of signing a message from a Gnosis Safe, unlike with an EOA where multiple tools exist.

We understand that many participants prefer to use Gnosis Safes to manage addresses with multiple keys for either personal OpSec reasons or when more than one individual is responsible for the decisions being made by an address, such as a delegate contract that is controlled by a team rather than an individual.

After consulting with the DUX team, we recommend the following process for multisig users to send messages using a Gnosis Safe Multisig. Please follow the instructions as written, as we cannot take any responsibility for any adverse outcomes if people do not follow the instructions verbatim. A worked example is provided as a demonstration. Please note that sending messages using this method will require a gas fee. This is due to limitations of Gnosis Safes and is not in the control of MakerDAO.

*Note that adding message signing functionality to Safes is actively being worked on, and this will hopefully be a short-term solution only.*

## Step-by-Step Instructions

### 1. Determine the Text of the Message You Want to Send

Are you communicating a CVC Decision, or simply verifying control of an address? Make sure the message text contains all of the required information for your use case. You will need to provide the exact text that you have included in your message for verification, so make sure you keep it safe.

For our example, we will be sending a message that contains the following text:

`T e s t`

### 2. Translate Your Message Text Into Hexadecimal

Use a text-to-hexadecimal tool such as [this one](https://www.rapidtables.com/convert/number/ascii-to-hex.html) to convert your message to hexadecimal.

 If using the linked tool, set Character Encoding to `ASCII` and Output Delimiter String to `None`.

In our example, we can see that the output string from our input of `T e s t` is `54206520732074`.

![](https://i.imgur.com/89lacmT.png)

### 3. Add the `0x` prefix

Add the prefix `0x` to your message.

In our example `54206520732074` becomes `0x54006500730074`.

### 4. Connect Your Wallet to Your Gnosis Safe

### 5. Open the Transaction Builder

Open the Transaction Builder App either by clicking the link on your Safe's homepage or by accessing the Apps menu.

![](https://i.imgur.com/RqyGH84.png)

### 6. Construct the Transaction

![](https://i.imgur.com/qNqBu3b.png)

Please note the following important points. The above image should be used as a reference.

1. **Ensure that Custom data is active.**
2. **Enter the "receiving" Ethereum address**. This address *must* be an EOA, not a multisig or contract address.  
    a. We *strongly recommend* that you use an address **that you control** in this section.
3. **Enter the ETH value for the transaction.**  
    a.  We *strongly recommend* that you set this to **0**.  
    b. If a non-zero value is selected and the transaction is executed, that amount of ETH will be sent from your multisig. **This could result in you losing your ETH, especially if you have not followed the advice in 2a.**
4. **Paste your hexadecimal message into the Data field.**  
    a. Make sure you have followed the instruction in section *3* of this guide.

### 7. Double Check Your Entries

Make absolutely sure that all the information is correct and you have followed all the steps above.

### 8. Click Add Transaction and then Create Batch

![](https://i.imgur.com/1zFN3vV.png)

### 9. Use the Simulate Function for a Sanity Check

If you see the Success message, then there are no issues with the data you entered.

**Note that this does not mean that you are not accidentally sending ETH if you have not entered `0` as the value in the previous steps.**

![](https://i.imgur.com/rINLpbJ.png)

If you see the following message, the transaction will fail, and your gas will be wasted. It is most likely that the recipient address is not appropriate. Remember to enter an EOA, not a multisig or contract address.

![](https://i.imgur.com/g4Zd70y.png)

### 10. Click Send Batch and Sign the Transaction From Your Wallet

### 11. Gather Signatures and Execute the Transaction

Other signers can review the transaction details before signing and executing the transaction.

The message data can be decoded and checked before execution using a hexadecimal to text tool such as [this one](https://www.rapidtables.com/convert/number/hex-to-ascii.html). Make sure to remove the `0x` prefix before pasting the hexadecimal message into the tool.

![](https://i.imgur.com/FsdVqd6.png)

### 12. Wait for Transaction to Execute

Once the transaction has executed the data can be accessed from the transaction on Etherscan.

- Click "Click to show more".

![](https://i.imgur.com/2kdS5Sb.png)

- Click "Decode Input Data"

![](https://i.imgur.com/3t4rNvr.png)

- Your message data is in the `2 data` field. There may be some extra `0`s on the end of the string - this is not a problem.

![](https://i.imgur.com/6ugZbEs.png)

### 13. Decoding the Message

Use a hexadecimal to text tool such as [this one](https://www.rapidtables.com/convert/number/hex-to-ascii.html) to decode your message. Remove the `0x` prefix before pasting the hexadecimal message into the tool.

The tool should reveal text that is identical to your input text from *1* and has been verifiably sent from your multisig wallet.

![](https://i.imgur.com/o9T24m1.png)

>Page last reviewed: 2023-08-03
>Next review due: 2023-11-03