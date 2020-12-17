# A Forensic Analysis of the BTC Economy 
## An attempt to predict what BTCs are spent on
This is the result of my final project of the Data Analyst Bootcamp at Ironhack


## Project Intro/Objective
Bitcoin is money on the internet, invented in 2009 by an unknown person called Satoshi Nakamoto. 
Every Bitcoin(BTC)-Addresse (a BTC addresse is comparable to a bank IBAN number), every transaction made on the Bitcon network is encrypted, the only thing made public is the amount transferred as well as the UNIX-timestamp the transfer was made. 

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

Those addresses were taken frome websites such as https://www.walletexplorer.com and bitcoinabuse.com and then labeled accordingly. 


In a next step I went through various datasets, 
https://senseable2015-6.mit.edu/bitcoin/
https://datahub.io/cryptocurrency/bitcoin
to look those labeled addresses and their corresponding transactions up. 

Each addresse can have an infinite amount of incoming and outgoing transactions, which each then can have a variable amount of inputs/ outputs. Therefore my 
newly created datasets scaled exponentially. At the end I managed to identify 2718 BTC addresses and 7.398.258  corresponding transactions, in which BTC was spent to one of the above mentioned sectors. To further be able to work with this data I grouped it by transaction received and amount received per day by BTC addresse. I did this for both the transactions received and the transactions sent out from the labeled addresse.

I then added metadata and filtered from the BTC ecosystem dara the corresponding day the transactions were made and collected metadata in order to train my ML model.  

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
- data collection
- data exploration
- data processing/cleaning
- statistical modeling
- model testing
- feature engineering
- hyperparameter tuning
- visualization
- writeup/reporting

