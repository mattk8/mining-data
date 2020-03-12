# Proof-of-Work Mining Data

**`global-device-estimates.xlsx`** is a model to estimate the number of mining devices deployed on the Bitcoin network at a given time.

The calculation divides total Bitcoin (BTC) hashpower by estimates of individual device capacity to generate hash power.

The WEIGHTED worksheet gives plugs for A, B and C as well as plugs to determine the relative weighting of A, B and C. This allows users to choose their own estimates, say high, medium, and low and choose the weight of those estimates to create a unified yearly hashpower estimate. 

**Future Additions/Improvements:**

* Make the variables bi-annually or quarterly.
* Bring in detail from `mining-devices.csv` to come to more precise estimates/plugs.
* Use the energy consumption data in `mining-devices.csv` and Bitcoin energy consumption data for an alternative method.

Sources
-------

| Filename             | Contents               | Data Points                                                                                    | Source                                                                      |
| -------------------- | ---------------------- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `mining-devices.csv` | Popular Mining Devices | Company, Device, Device Age, Hash Rate, Power Consumption, Year Released, Month Released, etc. | [F2 Pool](https://www.f2pool.com/miners?currency_code=btc)                  |
| `hash-rate.csv`      | Historical Hash Rate   | Date, Hash Rate (TH/s)                                                                         | [Blockchain.com ](https://www.blockchain.com/charts/hash-rate?timespan=all) |



Reference
---------

### Blockchain.com
* Hash Rate - Blockchain.com
    - The estimated number of tera hashes per second (trillions of hashes per second) the Bitcoin network is performing.
    - Source: [blockchain.com](https://www.blockchain.com/charts/hash-rate)
    - [All-Time Hash Rate](https://www.blockchain.com/charts/hash-rate?timespan=all)

### F2 Pool
* [F2 Pool - Popular Mining Devices](https://www.f2pool.com/miners?currency_code=btc)

### Bitmain
* [Application Proof of BitMain Technologies Holding Company](http://templatelab.com/bitmain-ipo-prospectus/)

### Canaan
* [Canaan Inc. American Depositary Shares (CAN) SEC Filings](https://www.nasdaq.com/market-activity/stocks/can/sec-filings)
* [Canaan Inc. - Form F1](https://secfilings.nasdaq.com/filingFrameset.asp?FilingID=13703543&CoName=CANAAN+INC%2E&eHTML=&FileName=&FilePath=&FormType=F%2D1&Market=&RcvdDate=10%2F28%2F2019&site=&sitesubtype=&Ticker=&View=html)

### Coinshares
* [Bitcoin Mining Network Update - December 2019](https://coinsharesgroup.com/research/bitcoin-mining-network-december-2019)
* [Bitcoin Mining Network Update - June 2019](https://coinsharesgroup.com/research/bitcoin-mining-network-june-2019)

### Other
* [Crypto Mining 101 - Overview & Landscape of the Mining Industry](https://www.chrismccann.com/blog/crypto-mining-101-overview-and-landscape-of-the-mining-industry) - Chris McCann
