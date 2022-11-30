
# ELECTRON RADIANT WALLET
## _Create multisign with 3 wallets and 2 need signers_

One of the new features of **ZEUS** and Electron Wallet 0.1.3 is the ability to use multi-signature wallets. Here is a basic process of its use.

## What is a MultiSig wallet? 
[https://www.bitstamp.net/learn/security/what-is-a-multisig-wallet](https://www.bitstamp.net/learn/security/what-is-a-multisig-wallet)
[https://www.coindesk.com/tech/2020/11/10/multisignature-wallets-can-keep-your-coins-safer-if-you-use-them-right](https://www.coindesk.com/tech/2020/11/10/multisignature-wallets-can-keep-your-coins-safer-if-you-use-them-right)


## Starting

#### Required
* Last version of Electron Wallet. I use  here version 0.1.3
* SO compatible with wallet: Wndows, Linux and Mac.
* Other wallets or persons to sign

#### Create wallets.
The first step is to create a new wallet. In this guide, a test will be done with 3 wallets where it will only be necessary to sign with two of them.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/01-create-wallet.png?raw=true)

Select Multi-signature wallet
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/02-select-multisign-wallet.png?raw=true)

In this section is where you select the type of multi-signature wallet. It is possible to make multiple possible variants, but here we will do the usual 2 out of 3.

- Total cosigners: 3
- Requiere signatures: 2
 

![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/03-select-number-cosigners-and-signatures.png?raw=true)

For the example I will create 3 wallets with 3 new seeds
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/04-new-seed-restore-or-priv-key.png?raw=true)

Very important to make a secure copy of the words or the funds in the generated wallet could be lost.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/05-new-seed.png?raw=true)

Master public key is what you need to add to the other portfolios to form the multisign wallet.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/06-master-pub-key.png?raw=true)

When adding cosigners it is necessary that the other two wallets tell you their master public key to continue creating the multisign wallet. 

**IMPORTANT: Never pass the seed to anyone, only the master public key.**
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/07-add-other-cosigner-master-pub-key.png?raw=true)

Create a good password to encrypt your wallet
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/08-password-wallet.png?raw=true)

### These are the data for the portfolio that I have created for the guide and can be used to review it

- **1 SEED:** tumble cage van bind device party shoe rail valid canal witness dial
- **masterpub-key:** xpub6CCA12nJkoBPVtZUswdEnVT9LR87zxutoKpSpA4crx9khyuupX4qsuWyswbZub63Dqhz7hRYfRZt4oPd6D9yherrjUYcmQmdguas99FcW5x
- **2 SEED:** avocado tuition asthma wine solar garbage limb play example hybrid unaware loud
- **masterpub-key:** xpub6D2CVbotwBsk7czNJQjKKWWa993PjTBJHG9fHV54yXoiPVPCZZwp6JNYUFD2PJQWfUAgjqueVwwx8nqfspGHYfmRj6FN1LCNz3wmK3hGiNR
- **3 SEED:** drift kitten flash alter update program island slide leisure youth spider diet
- **masterpub-key:** xpub6DJgWZhSCwU8VWQxnzpUky18gH9ZtvesYac2rVsbuyyeDyVsBxdgXF3GUDiic73eFsf5ioZTgwKRwyv4HLACjmnKQS3Pn4j9zhWFce3hmiG

The three wallets would look as shown in the image. The addresses of all the multi-signature wallets start with 3, this is correct.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/09-same-address-all-wallets.png?raw=true)

#### Send RXD to test wallet

I have sent 10.5 rxd for testing to the address: 3Be9yJ3qBuHVwEsCbptmxVykRhQcXwThC4
https://radiantexplorer.com/address/3Be9yJ3qBuHVwEsCbptmxVykRhQcXwThC4

When receiving funds in the first direction, all wallets display the message to receive funds at the same time.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/10-all-wallets-recive-same-time.png?raw=true)

And here you would see it in the wallets
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/11-all-wallets-recive-same-time.png?raw=true)

#### TEST MULTI-SIGN WITH OTHER CONSIGNER

Now it's time for the sending process with the signature of two wallets. A destination address is selected and the amount to be sent. This part does not change.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/12-send-with-one-wallet.png?raw=true)

The change is made when you click on send and a window appears with the transaction data. You can see that there is a signature of two and that it has been transferred to the network.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/13-transaction-broadcast.png?raw=true)

For the signature in another of the two wallets, it is necessary to copy the transaction as shown in the picture below
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/14-copy-tx-to-other-signer.png?raw=true)

And in the wallet of one of the other two wallets go to: **TOOLS > LOAD TRANSACTION > FROM TEXT**
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/15-past-tx-in-other-wallet.png?raw=true)

Here is pasted the transaction copied from the wallet that generated the sending
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/16-load-tx-in-other-wallet.png?raw=true)

Once accepted, a window with the transaction will pop up. Check that everything is OK and then click on **Sign** and **Broadcast** to send to the network.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/17-sign-and-broadcast-transaction.png?raw=true)

If all goes well, the window with the generated TX will be displayed
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/18-payment-sent.png?raw=true)

And in all the portfolios you will be able to see how the funds go to the selected address.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/19-tx-final-all-wallets.png?raw=true)

In wallet information appears data of the wallets involved in the multi-signature.
![](https://github.com/Antares-RXD/Radiant-Guides/blob/main/Create-multisign-wallet/img/20-info-all-wallets.png?raw=true)

#### FIN
And this is the process for multisigning in Radiant from Electron-Wallet 0.1.3

#### MORE ABOUT RADIANT

| Plugin | README |
| ------ | ------ |
| Web | [https://radiantblockchain.org](https://radiantblockchain.org) |
| Medium | [https://medium.com/@RadiantLayerOne](https://medium.com/@RadiantLayerOne) |
| Github | [https://github.com/RadiantBlockchain](https://github.com/RadiantBlockchain) |
| Twitter | [https://twitter.com/RadiantLayerOne](https://twitter.com/RadiantLayerOne) |
| Twitter Community | [https://twitter.com/RXD_Community](https://twitter.com/RXD_Community) |
| Discord | [https://discord.gg/dXMs6VCt6H](https://discord.gg/dXMs6VCt6H) |
| Telegram | [https://t.me/RadiantBlockchain](https://t.me/RadiantBlockchain) |

Antares
