---
filename: notes_btc-cost-of-production.md
created: 30 March 2020
---

[Bitcoin’s Cost of Production — A Model for Bitcoin Valuation](https://medium.com/coinmonks/bitcoins-cost-of-production-a-valuation-approach-for-bitcoin-dcd76951040a) - Data Dater (March 7, 2020)

# DataDater’s Bitcoin Cost of Production (CoP) Model
* One of the drawbacks of the energy-value equivalence model lies in its ignorance of including capital expenditure (CapEx) as part of the process to arrive at the cost of mining Bitcoin.
    - CapEx for bitcoin mining would imply the cost of purchasing a mining rig, setting up farm infrastructure, regulatory/legal expenses, etc.
    - Also, the operating expenditure (OpEx) would include labor expense and pooling fees in addition to power expense, which the model ignores.
* Therefore, the CoP model attempts to compute both the CapEx and OpEx involved in mining bitcoins. The process is explained below:

## Calculating CapEx
* The model is developed from data post-May 2011, as Field-programmable Gate Array (FPGA) miners were introduced about then. **Also, the model assumes that the mining pool tends to use the most efficient rig (for obvious competitive reasons), hence the Antminer rigs are referred to for most parts in this valuation process.**
* Data pertaining to cost and ratings of the currently in-use Antminer rigs have been obtained from the Antminer website while those of their legacy counterparts from e-commerce sites such as Amazon or Alibaba.
* An average rig has a **lifespan of about 2–3 years**, hence the purchase cost is adjusted for depreciation using the _**declining-balance depreciation method**_.
* Further, in most cases, newer rigs are introduced before a previous model runs its lifespan, as a result, the effective cost of the previous rig depends on the number of bitcoins it hs mined till the time of its replacement. This is called the _**units-of-production depreciation method**_.
    - For instance, the S3 was in use for approximately 153 days (July 2014 to December 2014) and mined an average of 0.97 bitcoins in that period. Hence, its effective purchase price was $299/0.97 = $308.24. It is to be noted that the model assumes that the entire mining network has been taking the same time to switch from one rig to the next released rig for all rig releases.

## Calculating Opex
* To calculate the cost of electricity for mining bitcoins, **data of the network hashrate and daily coin issuance, are fetched from Coinmetrics**.
    - From this, the number of hashes required to mine 1 bitcoin is calculated as _**Hashrate/Daily Issuance**_.
    - This value is then divided by the mining righashrate to obtain the **time required to mine 1 bitcoin in an hour**.
    - This time value is multiplied by the **power rating of the rig** to obtain the _**number of units in kWh required to mine 1 bitcoin**_.
    - Finally, this unit count is **multiplied by the cost of consuming electricity in US Dollars** to obtain the cost of electricity to mine 1 bitcoin.

### Example
* To illustrate the above-mentioned method, the daily network Hashrate on 13 October 2014 was 266,217.37*60*60*24 Tera hashes and 3,875 bitcoins were mined on that day.
    - Thus, (266,217.37*60*60*24)/3875 = 5,935,788.59 hashes were required to mine 1 bitcoin.
* The S3, with a hashrate of 0.43 Th/s would have taken (5,935,788.59/0.43)/(60*60) = 3.84 hours to mine than bitcoin.
* Given, the power rating of the prevalent S3 to be 339.57 W and an average global cost of electricity being $0.06, this could have incurred a cost of 3.84*339.57*$0.06 = $78.12.
* Therefore, the total cost of mining 1 bitcoin on 13 October 2014 was CapEx + OpEx = $308.24 + $78.12 = $386.36. This is close to the actual price of $391.99 on that day.
* Do note that miners most likely purchase the rigs at a discount and probably pay less tariffs for electricity, but this discount is offset by additional costs of infrastructure, labor, pool fees, and other overheads.
    - For the sake of simplicity, these costs have been ignored and the mining-rig price and tariffs have been taken as they have been.
