<h1><img width="30" src="http://i.imgur.com/Nq2lvZj.jpg"> Ethereum Point of Sale</h1>
https://ethereumpos.com

EthereumPOS.com is geared towards letting developers and merchants accept Ethereum (ETH) on their website or application. 
Using a simple QR code, the purchaser can scan the Ethereum Wallet and pay the expected amount for their purchase to be complete.

[EthereumPOS API Documentation](https://docs.ethereumpos.com)

##### EthereumPOS Mainnet API Endpoint
```
https://api.ethereumpos.com
```

##### EthereumPOS Ropsten Testnet API Endpoint
```
https://testapi.ethereumpos.com
```

# Why and What
EthereumPOS is a Point of Sale system for merchants and developers who want to accept Ethereum on their website or application. 
Using Ethereum blockchain you'll be able to confirm transactions quicker than with the bloat of the Bitcoin blockchain. EthereumPOS allows online shopping carts and applications to receive a callback to confirm the customer paid in full.

<img src="https://ethereumpos.com/images/payment.png">

# Payment Process
Ethereum POS is ment to be simple, and have a KISS principle API so many plugins can be built using HTTP post/get requests.

#### 1. Customer Payment
Once your application creates a total for that order, the customer will need to pay the expected amount for the transaction to process. 

#### 2. Payment Submitted
The customer pays the expected amount to the wallet shown, the transation is marked as *paid* once there is 1 confirmation. At this point, the customer will see a 'PAID' alert and a callback will be POST-ed to your endpoint. 

#### 3. Payment to Merchant
Once there are 12+ confirmations the entire balance of the wallet will be sent to the merchant/developer. A POST callback will be send to the merchants application and the order should be marked as 100% paid. 

# Transaction Fees
### Ethereum Fees
Type | ETH Cost | Comment
--- | --- | ---
Incoming Payment | 0 | Customer pays transaction fee
Payment To Developer | 0.00042 | Wallet pays transaction fee

### EthereumPOS Fees
Transaction Value | Fee Percent | Maximum Fee
--- | --- | ---
$1 - $1000 | 0.01% | 0.01 ETH
$1000 - $5000 | 0.008% | 0.01 ETH
$5000+ | 0.004% | 0.01 ETH

# Speed
Thankfully, Ethereum's network is pretty fast. Every 15-60 seconds a block gets broken and hopefully the users transaction is in the next block. When an order has 1 confirmation, it is marked as 'paid' for the customer. 

<img src="https://ethereumpos.com/images/payment2.png">

# Security
Each order/transaction is a new wallet with an encrypted password that is automatically locked. Once an order is placed, customer pays the expected amount, and 12+ confirmations on the payment, the ethereum wallet will unlock for 15 seconds and send the entire wallet balance to merchant. After the transaction is complete, the wallet will not be reused. 

# Possible Issues
Using the Ethereum network can be slow at times.

### Slow Confirmations
The customer might be waiting for their payment to clear because EthereumPOS requires 1 confirmation to be marked as 'paid'. 1 confirmation all depends on the transaction fee they put into the transaction. Coinbase currently sets the fee to 0.00042 ETH, which will get confirmed very shortly. Technically a customer could pay the expected amount, but have a low transaction fee around 0.0001 which will make 1 confirmation happen in around 1-5 minutes.

### Expected Amount too Low/High
If a customer pays the wallet more than expected value, Ethereum POS will refund the surplus of the wallet balance to the sender.  

Example: Customer pays 3.25 ETH but expected amount is 3.00 ETH. The wallet will send 3 ETH to the merchant and the remaining balance is sent back to customer. (less for transaction fee -0.00042 ETH)

Example: Customer pays 2.80 ETH but expected amount is 3.00 ETH. The wallet will refund the entire balance 2.80 ETH back to sender. (less for transaction fee -0.00042 ETH)

# Desktop Applications
EthereumPOS will have a Windows, Linux, and Mac application that will serve as a simple to use Point of Sale system.

# Mobile Applications
Along with desktop applications, Ethereum POS will have a mobile application on iPhone, iPad, and Android phones/tablets.

# Error Handling and Logs


<center>
<img src="http://i.imgur.com/Nq2lvZj.jpg"> 
</center>
