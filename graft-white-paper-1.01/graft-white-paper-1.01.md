# Graft
## Decentralized Global Merchant Payment Processor


Slava Gomzin

Dan Itkis



Version 1.01



## Table of Contents
### [Abstract](#Abstract)
### [Background](#Background1)
#### [The Value of Decentralized Payment Processing](#TheValue)
### [Terminology](#Terminology)
### [Transaction Fees](#TransactionFees)
#### [To Fee or Not to Fee](#ToFeeorNottoFee)
#### [GraftTransaction Fees](#GraftTransactionFees)

# Abstract <a name="Abstract"></a>
Graft is a global, open-sourced, blockchain-based, decentralized payment gateway and processing platform that anyone can use.
Any buyer and merchant can use Graft in a completely decentralized and inexpensive way. Graft ecosystem is open so anyone can participate by maintaining Graft blockchain and implementing network services.

Graft employs payment processing protocols and flows similar to traditional electronic payment systems such as credit, debit, and prepaid cards, which are already familiar to and trusted by millions of users and merchants around the world. This approach enables easier and faster adoption of Graft as a mainstream payment platform, while eliminating the need in centralized intermediaries (payment gateways and processors) currently required to facilitate transactions between buyers and merchants.

# Background <a name="Background1"></a>
Bitcoin[1] was created as an “online cash” - very secure but relatively slow settlement system which was unable to replace payment cards online or compete with both plastic cards and paper cash in brick-and-mortar stores (Figure 1).

![Bitcoin Transaction Processing without Centralized Intermediary](https://github.com/graft-project/graft-white-paper/blob/master/graft-white-paper-1.01/images/Figure%201.png "Bitcoin Transaction Processing without Centralized Intermediary")
**Figure 1:** Bitcoin Transaction Processing without Centralized Intermediary

Even though some existing cryptocurrencies[2] have improved confirmation times, they are still unable to process essential transactions types such as authorization and completion, which makes their adoption by retail, hospitality, and convenience store industries impossible without using intermediaries - payment processors and gateways[3] - who fill the gap (Figure 2). However, the very existence of payment processor, which is typically a centralized commercial organization regulated by government and controlled by shareholders, as an element of crypto payment transaction contradicts the fundamental principles of cryptocurrencies: decentralization, privacy, and independence. 

![alt text](https://github.com/graft-project/graft-white-paper/blob/master/graft-white-paper-1.01/images/Figure%202.png "Processing Bitcoin Transaction by Centralized Intermediary")
**Figure 2:** Processing Bitcoin Transaction by Centralized Intermediary

Most merchants are unable to accept cryptocurrencies without third-party payment processor due to uniqueness of the way blockchain networks process transactions, which is conceptually different from traditional electronic payment methods such as payment cards or Paypal. Although the overall concept of plastic card payments may have been outdated, there are technologies developed around them that accumulated enormous amount of merchant experience and user trust which cannot be abandoned overnight. Those technologies include real-time authorization protocols and smart cards.
There are several major differences between the ways traditional and cryptocurrency payment systems handle transactions, which in most cases make cryptocurrencies less attractive for merchants and/or consumers. Here is the list of technical limitations and business flaws of the existing cryptocurrencies comparing to traditional electronic payments: 

* Lack of Essential Transaction Types
* Unsuitable Payment Flows
* Long Confirmation Times
* Unbalanced and Unpredictable Transaction Fees
* Inability to Process Micropayments and Repeating Charges (Subscriptions)
* Lack of Offline Transactions support
* Low Scalability
* Volatility
* Incomplete Security
* Lack of Privacy Due to Traceability of Blockchain 
* Lack of Trust between Buyer and Merchant
* Questionable Utility
* Poor Usability of End-User Interfaces
* Lack of Customer Support 

By addressing all those issues, Graft elevates crypto payment processing to a new level, and makes possible their wide acceptance by mainstream merchants and consumers for the first time without violating the fundamental principles of cryptocurrencies. Let’s review each of those issues with greater detail and see how Graft addresses them.

## The Value of Decentralized Payment Processing <a name="TheValue"></a>
Why would a buyer want to start using cryptocurrency instead of (or in addition to) plastic cards or PayPal or Apple Pay, and why would a merchant want to accept cryptocurrency in addition to (or instead of) existing payment methods? Obviously, if we don’t find the right answers to those simple questions, there is no point to create this document.

While the answer to the first part of this question may consists of several elements as there might be multiple reasons (and combinations of them) to individuals to keep their money in a form of cryptocurrency, the answer to the second part of this question is relatively simple. Merchants always want to extend their customer base to increase their revenues, and if they identify a significant group of potential customers who prefer, for any reason, to use cryptocurrency, they will start accepting cryptocurrency. And Graft provides a unique opportunity for merchants to accept crypto payments from their buyers without any middlemen and with near zero fees. 

However, there may be additional value. In some cases, merchant might want to know the real identity of the buyer in order to comply with laws and regulations, for example, to make sure the buyer is older than 21 to be allowed to purchase some items. 

Since Graft is both decentralized payment processor and cryptocurrency, it is able to facilitate the full payment cycle without other cryptocurrencies or assets involved. However, in addition to decentralization and right for privacy, there is a freedom of choice which is another important fundamental liberal principle. Moreover, there might be a commercial need for diversity of cryptocurrencies for both buyers and merchants. Therefore, Graft will support Bitcoin and several major cryptocurrencies as additional choice for buyers and acceptable method of payoff for merchants. This feature will eliminate the need for merchant to integrate with multiple (centralized) payment software providers, and for user to sign up for centralized services and learn and maintain multiple wallet apps. It is important to note that merchants will have to accommodate higher risks and additional expenses associated with acceptance of alternative cryptocurrencies due to their slower confirmation times and higher transaction fees. 

# Terminology <a name="Terminology"></a>
### Graft 
1. **G**lobal **R**eal-time **A**uthorizations and **F**und **T**ransfers - decentralized global open platform for processing  real-time authorizations and settlements of merchant payments and fund transfers using untraceable blockchain, decentralized API, and open community of service brokers that support variety of payment and payout methods including cryptocurrencies and traditional credit cards and bank transfers. 

2. A plant that has a twig or bud from another plant attached to it so they are joined and grow together.[4] Grafting is an advanced technique that botanists, farmers, gardeners, and hobbyists use to add living tissue from one plant to another. Why would anyone go to all this trouble of attaching two bits of plants together? Well, it turns out that this technique has a lot of benefits. Growers can choose different parts of plants that have particular attributes, and attach them to other plants. Let's say a certain tree has really strong roots, but its fruit isn't so great. This tree would make great rootstock, or a plant selected for its roots. It can be combined with another tree that doesn't have good roots, but produces wonderful fruit. Plants that are selected for their stems, flowers, or fruit are called the scion. A desirable scion can be grafted onto a strong rootstock to create a truly great tree. This is pretty common practice in the gardening industry. It allows for plants to grow in many new areas, and gives us access to more products.[5]

### Supernode
Independant always-on server running implementation of Graft Blockchain node and Graft DAPI, and maintaining the blockchain via block mining, processing of real-time authorization and settlement DAPI calls between buyers and merchants, and hosting additional services such as instant cryptocurrency exchange, credit/debit card acceptance, and merchant payouts in local currency.    

### Service Broker
Graft protocol extension hosted on supernode or a group of supernodes and owned by the supernode operator. Service Brokers implement special additional features that cannot be automatically executed by fully decentralized network or/and requires special regulation framework such as PCI DSS[6] or NIST 800-63-3.[7] Examples of service brokers are credit card payment acceptance broker and bank payout transfer broker.   

### Domain
Virtual decentralized independant “merchant account” where merchants can set up authorization and payout rules and triggers that will have an affect on transactions for that specific merchant.

### graftcoin
Native cryptocurrency supported by Graft blockchain and used for real-time payment authorizations, funds transfers, and settlement between buyers and merchants.

### DAPI
Decentralized stateless API implemented by supernodes in order to support lightweight client apps such as Graft Wallet, Graft Point of Sale, and third party point of sale apps and shopping cards.
Graft SDK
Source code provided to third party point of sale and wallet application vendors for facilitating an integration with Graft.  
### Graft Wallet
“Lite" desktop, mobile, and browser extension apps that allow making payments and fund transfers using graftcoins, other major cryptocurrencies, or credit/debit cards by calling Graft DAPI.

### Graft Point of Sale
“Lite” desktop and mobile apps that allow merchants accepting payments in graftcoins, bitcoins, altcoins, or credit/debit cards; issuing and redeeming gift certificates, loyalty reward points, and store credits; configure settlement payouts in graftcoins, bitcoins, altcoins, or local fiat currencies.
 
# Transaction Fees <a name="TransactionFees"></a>
Why is it necessary to have a transaction fee in the first place? After all, there is no commercial enterprise behind the blockchain, so why would users need to pay fees, who does collect them, and how much should they charge? 

## To Fee or Not to Fee <a name="ToFeeorNottoFee"></a>
Multiple powerful nodes (servers) distributed throughout the world are required in order to support secure and highly available cryptocurrency network. So who is going to maintain these servers, and what's the motivation and incentive for maintaining the blockchain node? In Bitcoin and other cryptocurrency networks, the funding is achieved through mining and transaction fees - the node owners make money on mining new coins from each block as well as getting fees for each transaction. 

The mining has another purpose: constant and steady injection of new coins into the system to keep up the liquidity with the growing demand for extra coins as the acceptance widens and usage increases. As the system get traction, the node operators will receive more revenue from transaction fees, so the bonus for mining can be gradually reduced with each new block to limit the overall supply.

In ideal world, the cryptocurrency should be available for everyone and free of charge. In fact, there are networks that promise free transactions.[8] In other networks, including Bitcoin, the fees are used to prioritize transactions and “resolve” the scalability problem.

In Graft network, however, the fee is used for two reasons. First, to avoid network abuse and associated performance and blockchain size issues. For example, using the real network for testing. If transaction is completely free, one can move the same amount between two accounts indefinitely. Second, to become the only incentive for node operators after the mining bonus becomes too small. 

### Charging the Wrong Guy
The problem with Bitcoin and other cryptocurrencies’ fee is that they charge the wrong side of the transaction. It’s even worse than traditional card payments because unlike plastic payments, both buyer and merchant pay fees for cryptocurrency transaction: the buyer pays to the cryptocurrency network, while the merchant pays to the payment processor.[9] The (average/layman) payer is often confused by the process which looks more like a betting, without clear explanation of the fee schedule, which obviously does not make cryptocurrency payments very attractive. 

### Micropayments: How Do I Pay with Crypto for a Cup of Coffee? 
Another problem currently experienced by Bitcoin is its inability to handle micropayments due to high transaction fees.10 Graft resolves this problem by introducing a unique (in cryptocurrencies world) approach to transaction fees.

## Graft Transaction Fees <a name="GraftTransactionFees"></a>
Graft reintroduces convenient fee structure with no fees for the payer so all fees are paid by the receiver (merchant), just like everyone used to do with traditional electronic methods of payment. Graft makes micropayments accessible to everyone by setting very low (comparing to credit cards11 and online payment processors,[12] and other cryptocurrencies[13]) fees, but without fixed fee component (Table 1). All fees are paid by the payees.  
 
**Table 1:** Graft Network Transaction Fees

Micropayments (less than 10 GRF) | Regular Payments (more than 10 GRF)
--- | ---
0.1%  | 1% of log10 (significantly less than 0.1% as transaction amount grows)               
     
The logarithmic fee schedule allows creating incentive for processing less transactions with small amounts (i.e. combining multiple transactions together whenever possible) while keeping low transaction fees for large transaction amounts (Table 2).

**Table 2:** Examples of Graft Network Transaction Fees

Transaction amount | Transaction Fee Amount | Effective Transaction Fee
--- | --- | ---
0.01 GRF | 0.00001 GRF | 0.1%
1 GRF | 0.001 GRF | 0.1%
10 GRF| 0.01 GRF | 0.1%
50 GRF | 0.01699 GRF | 0.03398%
100 GRF | 0.02 GRF | 0.02%
1,000 GRF | 0.03 GRF | 0.003%
1,000,000 GRF | 0.06 GRF | 0.000006%

### Additional Third Party Service Broker Fees
When accepting different payment methods such as bitcoins, altcoins, credit/debit cards, or processing merchant payouts in different currencies such as bitcoins, altcoins, or local fiat currency, additional payment broker and/or payout broker fees may be applied. These are not hidden fees as they are published by the brokers at the time of merchant sign-in for the broker service. Those fees are always charged to the merchant at the time of transaction settlement (payout), i.e. there are no any setup, upfront, or periodic fees.

### Customer Fees
Some cryptocurrencies such as Bitcoin require customer to add transaction fee in order to get fast confirmation. Such fees are configured by customer wallet application and paid by customer. Most Bitcoin users are already accustomed to such fees. 

### Paying Fees Using Margin Balances
In some cases, transactions fees can be charged using special “margin” balances provided by Graft network itself or/and margin brokers. Examples of such transactions are Issue and Redeem transactions related to gift certificates, loyalty rewards, and store credit processing. This is done in order to allow merchant transaction processing even if the merchant does not have enough balance on Graft account yet. 
 
# Transaction Processing 
The world’s moving towards “thin” devices. People around the world use more smartphones and tablets and less workstations and laptops. Therefore, decentralized crypto payment system cannot rely solely on small individual nodes hosted on personal computers but rather should be based on dedicated powerful supernodes hosted by professionals, with thin clients apps connected to a quorum - a group of supernodes randomly selected by special fraud-prevention algorithm - via DAPI calls.

## Confirmation Time: Introducing Real Time Authorizations
Long confirmation time[14] (from several minutes to several hours, depending on transaction fee[15]) is one of the main reasons for low adoption of cryptocurrencies in retail and hospitality sectors where customers cannot wait and so merchants must process payment instantly. Unlike some other cryptocurrency networks that tried to resolve this problem by introducing special add-on systems or transaction types16, Graft processes all its transactions in real time (less than 3 seconds), without charging an extra fee or compromising the principle of decentralization (see Figure 3). 


