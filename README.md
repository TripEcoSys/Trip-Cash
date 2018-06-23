## Welcome to world's largest decentralized travel eco-system "TripEcoSys"

We are proudly presenting “TripEcoSys” world’s largest decentralized tourism ecosystem powered by Ethereum Blockchain. Where people can find every travel related service provider under one roof and also can earn money by sharing their valuable contents. Our goal is to revolutionize the tourism industry by improving the traditional.Travel Eco System (TES), for the purpose of connecting consumers directly with service providers in a decentralized way with help of emerging Blockchain technology.

## Mission and vision of  -TripEcoSys (TES).

The mission of TripEcoSys is to make a fully decentralized travel ecosystem where every people from around the world to have a carefree travelling and enjoy personalized approach to their travel needs with authentic experience wherever they go. Encouraging every member by incentivized their contribution of time, skill, local experience and resources.

Our platform mainly consists of :

* Travel blog : An  incentivized,  blockchain-based,  public  content sharing platform.
* A social travel review platform built on blockchain in order to bring fairness to all content creators in form of financial rewards.
* Specialized ad platform for travel service providers like hotels and restaurants, airlines, car rentals, tour guides, travel goods seller etc.
* Multi signature wallets for securely storing and spending your tokens.
* Decentralized public exchange for securely exchanging your desired coins and token. 

# Project Overview

![Project Overview](https://i.redd.it/knbcr7szh5511.png)

“TripEcoSys” is a decentralized travel ecosystem  that supports community building and social interaction with cryptocurrency rewards. “TripEcoSys”  combines concepts from social media with lessons learned from building cryptocurrencies and their communities. An important key is to inspiring participation in any community, currency or free market economy is a fair accounting system that consistently reflects each person's contribution.

 “TripEcoSys”  is the world’s first largest decentralized platform that aims to combine a incentivized  social travel blogging system, an exchange, a multi-signature wallet and a merchant payment gateway in one place to meet all the necessity of traveler’s worldwide, accurately and transparently who make  subjective  contributions  to its  community.

# The Token

Blockchain as distributed ledger, opened the gates of opportunities for real-time online payment solutions. Adoption of this technology in travel industry has always been on the digital currency side giving us just another way of payment for our reservations. Although this is avery important feature as the payments no longer would need extra fees there is an unseen cost-machine at the back of the transactions thus explaining the higher prices. We believe that blockchain technology and digital currencies will eventually solve the transaction fee problem.To take it a step further, we will redefine how the travel product is defined and consumed while providing a real-time solution for BSP. Let’s take a further look.

## Further Solution (TripPay)
![TripPay](https://i.redd.it/a6sgfmww0q511.png)

TripPay(TCH) is a ERC20 compatible token based on Ethereum. Blockchain, in its nature, offers a basic and fundamental solution. It is the immutable history of the transactions and thus expressing the final ownership of the assets. Assets can be money, a license or a ticket. Its elegant design in keeping a secure, distributed chain of information would help real business scenarios as discussed in the former section. The key points further is aiming to achieve are.
Real-time settlement :

* Decentralizing the process of settlement, thus removing the mediator.
* Reducing the amount of money kept or blocked in deposit or safety accounts.
* Cost reduction on payments.
*	Simultaneous cross-border payments.
*	Customizable travel asset.
*	Interoperability like merger, divide, exchange of the travel assets.


_The digital coins used by TripEcoSys are not registered by any government, its function is subject to the trust of its users, everything flows according to supply and demand. The cryptocurrency that we will use will be the TripPay(TCH) token._

# TripEcoSys Multi-Signature Wallet
The purpose of multi-Signature wallets is to increase security by requiring multiple parties to agree on transactions before execution. Transactions can be executed only when confirmed by a predefined number of owners. 

**Features**
*	Can hold Ether and all kind of tokens with Multi-Signature support.
*	To stop one person from running off with the loot.
*	To reduce key person risk in case one person is incapacitated or loses their keys.
*	Easy to use offline signing (cold wallet) support.
*	Integration with web3 wallets (Metamask, Mist, Parity, etc).
*	Optional email notifications when an event is triggered or you are required to sign a transaction.
*	Interacting with any contracts with UI support.
*	Hardware wallet support (Ledger Wallet).
*	Transaction data and log decoding, makes transactions more readable.

# What will be our approach towards Ethereum Multisig Standard?

At its core, a multi-signature wallet needs

* A list of people who are allowed to do things.
*	Rules on how many of those people have to agree before it happens.
*	A way to receive ETHER.
*	A way to submit a request.
*	A way to agree to a request (and submit it if you are last).
*	A way to re-submit the request if it fails.

There is a load of nice to have as well, but that is enough to get started.
Recent events have brought Ethereum multi-signature wallets (a.k.a. “multisigs”) under the spotlight. Twice this year, hackers or general troublemakers have exploited vulnerabilities in the ‘Parity multisig’ smart contract. Critics have been quick to cite these incidents when suggesting Ethereum can’t work due to a large attack surface, but the reality is much more nuanced.

TripEcoSys is currently holding a token sale and is stashing its funds in a secure offline setup. When weighing our storage options, we immediately decided against all multisig smart contracts with which we were familiar, specifically those made by: Parity, Ethereum Foundation, ConsenSys, and Gnosis. This is not to say that all these wallets are exploitable (Gnosis’ wallet, for example, has held $200M for over a year without a breach), but the decision came from general prudence regarding complexity. None of these wallets met our needs, but that is not to say such a wallet cannot exist on Ethereum.

As a means of comparison, we can look at Bitcoin’s P2SH-based multisignature scheme, which has zero reported hacks since its first use in 2012. The difference in security indeed comes from a reduced attack surface, though this is largely by necessity in Bitcoin’s constrained scripting language.

So let’s see how we will draw parallels between Bitcoin’s multisigs and a proposed Ethereum Multisig.

**Bitcoin Multisig Wallets**
Before exploring Ethereum, it is instructive to first understand how Bitcoin’s pay to script hash (P2SH) scheme works and how it applies to a multisig scheme. The formal P2SH definition can be found in BIP16. The steps are roughly as follows:
1.	Generate a multisignature address based on a set of public keys and a “threshold” parameter, which is the minimum number of signatures required to trigger a spend.
2.	Fund the new multisig address. This will produce a UTXO (unspent transaction output) owned by the multisig address.
3.	Create a new, raw offline transaction spending the multisig’s UTXO.
4.	Sign the raw transaction with one private key. This will return a hex string.
5.	Sign the hex string with another private key. This will return a new hex string.
6.	Continue step 5 until the threshold is met (e.g. 3 signatures out of 5). Send the result in a script with the UTXO to spend. The bitcoins will transfer to the desired recipient.

**Extending to Ethereum**

If the goal is to emulate Bitcoin’s multisig scheme on Ethereum, we can learn a lot from the previous section. We need to create a multisignature scheme with no extraneous functionality and no in-between state. In other words, there can only be two outcomes to our multisig execution: make a transaction or do nothing.
Note that Ethereum’s transactions are account-based rather than UTXO based, so they are more complex. By “make a transaction” I mean sign an arbitrary set of data to a specified address (which can be a contract address) with a specified value (i.e. amount of ether). In Solidity, this is represented as:
destination.call.value(value)(data)
Another important property of Bitcoin multisigs is their instantiation. Once created, multisigs cannot be changed. This means that the owners of the contracts and the threshold parameter have been frozen forever. The Ethereum parallel would be to create an immutable state upon instantiation.
To summarize, we want the following attributes in our Ethereum multisig:
1.	Binary outcome — either accept the transaction or fail immediately.
2.	Restricted functionality — the wallet can make transactions, but it can’t do anything else.
3.	Creation finality — parameters are locked once the wallet is created.





