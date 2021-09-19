# A Forensic Analysis of the BTC Economy 
## An attempt to predict what BTCs are spent on


## Project Intro/Objective
Bitcoin is money on the internet, invented in 2009 by an unknown person called Satoshi Nakamoto. 
Every Bitcoin(BTC)-Addresse (a BTC addresse is comparable to a bank account number), every transaction made on the Bitcon network is encrypted, the only thing made public is the amount transferred as well as the UNIX-timestamp the transfer was made. 

However, some BTC-addresses have been identified, either because they are published by the entity owning these addresses themselves or because they could have been identified during criminal investigations, etc. 

In this project I attempt to use those identified addresses to cluster out certain sectors of the BTC Economy. Namely:

*Exchanges
*Payment Service Providers
*Gambling
*Illicit Activties, such as Dark Net markets
*Mining

Exchanges are portals, where Bitcoin users can trade their BTCs to other cryptocurrencies or fiat money, such as USD or EUR. An increase in transactions being sent to addresses belonging to exchanges therefore indicate an increase in trading activties for BTCs.
Payment Service Providers can be merchants that accept Bitcoins for their products. It can be service providers that enable APIs, POS Interfaces and therelike for e-commerce businesses to use Bitcoin. It can also be credit cards and other financial services that deploy Bitcoin. 
Gambling is self-explanatory.
Illicit activties are portals on the Dark Net, where users can buy drugs and other illicit products using Bitcoin. 
Scams refer to the unfortunate 

Those addresses were taken frome websites such as [walletexplorer.com](www.walletexplorer.com) and [bitcoinabuse.com](https://bitcoinabuse.com) and then labeled accordingly. 

In a next step I went through various datasets, 
[MIT.edu](https://senseable2015-6.mit.edu/bitcoin/), 
[Datahub.io](https://datahub.io/cryptocurrency/bitcoin)
to look those labeled addresses and their corresponding transactions up. 

Each addresse can have an infinite amount of incoming and outgoing transactions, which each then can have a variable amount of inputs/ outputs. Therefore my 
newly created datasets scaled exponentially. At the end I managed to identify 2718 BTC addresses and 7.398.258  corresponding transactions, in which BTC was spent to one of the above mentioned sectors. To further be able to work with this data I grouped it by transaction received and amount received per day by BTC addresse. I did this for both the transactions received and the transactions sent out from the labeled addresse.

I then added metadata and filtered from the BTC ecosystem data on the corresponding day of the transactions. I then used the newly collected metadata in order to train my ML model.  

### Description of the Data

Both datasets 

***Transfer Date*** - Date the transaction was included into a block and hence transferred

***Addresse*** - Receiving BTC addresse

***number_of_txin*** - Number of transactions a labeled addresse receives per day

***income*** - The sum of income each labeled addresse receives per day, denominated in Satoshi (1 Satoshi = 1e-8 BTC)

***sector_txin*** - The respective sector of the BTC addresse

***txVolume(USD)*** - On-chain transaction volume. A broad and largely unadjusted measure of the total value of outputs on the blockchain, on a given day. This is an answer to the question “approximately how much value, denominated in USD, circulates on the Bitcoin blockchain a day?”

***Price*** - BTC price from CoinMarketCap

***exchangeVolume(USD)*** The dollar value of the volume at exchanges like GDAX and Bitfinex.

***generatedCoins*** - This refers to the number of new coins that have been brought into existence on that day, which can be interpretated as the inflation rate. 

***fees*** - Fees paid for transactions, based on the native currency, not USD. 

***activeAddresses*** -  The number of unique sending and receiving addresses participating in transactions on the given day.

***averageDifficulty*** - Average measure of how difficult it is to find a hash below a given target. The Bitcoin network has a global block difficulty. Valid blocks must have a hash below this target. Mining pools also have a pool-specific share difficulty setting a lower limit for shares. This figure is relevant for the mining industry. 

***paymentCount*** - A more accurate figure than the txcount. Into each transaction various inputs and outputs can be bundled in, in order to save block memory and transaction fees. A practice that is often used by exchanges and big payment services, which have to make many transactions at once. Payment count for UTXO coins is defined as sum of outputs’ count minus one for each transaction. We assume that transaction with N outputs pays to N – 1 addresses and the last N-th output is change. Transactions with only one output do not contribute to payment count, as they are likely to be a self-churn. 

***medianTxValue(USD)***  -The median value of a transaction on a given day.

***medianFee*** -Median transaction fee on a given day. 



### Methods Used
* Descriptive Statistics
* Inferential Statistics
* Machine Learning
* Data Visualization
* Predictive Modeling

### Technologies
* Python
* Tableau
* Pandas, jupyter

## Needs of this project
- Data collection
- Data exploration
- Data processing/cleaning
- Statistical modeling
- Model testing
- Feature engineering
- Hyperparameter tuning
- Visualization
- Writeup/reporting

## Featured Notebooks/Analysis/Deliverables
* [Notebook Regression Modell](https://github.com/Lizzl/Predicting-BTC-spendings/blob/main/A%20Forensic%20Analysis%20of%20the%20BTC%20Economy.ipynb)
* [Tableau Visualizations](https://public.tableau.com/profile/alice.kohn#!/vizhome/The_BTC_Economy/BTCEconomyin2018?publish=yes)
* [Clean Dataset as CSV](https://github.com/Lizzl/Predicting-BTC-spendings/blob/main/BTC_Spending_Analsis.csv)
* [Presentation](https://github.com/Lizzl/Predicting-BTC-spendings/blob/main/Presentation.pdf)
