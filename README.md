# Ethereum Point of Sale
#### EtherereumPOS.com

EthereumPOS.com is geared towards letting developers and merchants accept Ethereum (ETH) on their website or application. 
Using a simple QR code, the purchaser can scan the Ethereum Wallet and pay the expected amount for their purchase to be complete.

# Payment Process
Ethereum POS is ment to be simple, and have a KISS principle API so many plugins can be built.

#### 1. Customer Payment
Once your application creates a total for that order, the customer will need to pay the expected amount for the transaction to process. 

#### 2. Payment Submitted
The customer pays the expected amount to the wallet shown, the transation is marked as *paid* once there is 1 confirmation. At this point, the customer will see a 'PAID' alert and a callback will be POST-ed to your endpoint. 

#### 3. Payment to Merchant
Once there are 12+ confirmations the entire balance of the wallet will be sent to the merchant/developer. A POST callback will be send to the merchants application and the order should be marked as 100% paid. 

# Speed
Thankfully, Ethereum's network is pretty fast. Every 15-60 seconds a block gets broken and hopefully the users transaction is in the next block. When an order has 1 confirmation, it is marked as 'paid' for the customer. 

# Security
Each order/transaction is a new wallet with an encrypted password that is automatically locked. Once an order is placed, customer pays the expected amount, and 12+ confirmations on the payment, the ethereum wallet will unlock for 15 seconds and send the entire wallet balance to merchant. 

# Error Handling and Logs
