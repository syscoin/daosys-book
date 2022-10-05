# Product RoadMap

### SYS Labs

SYS Labs is the R\&D development arm of the Syscoin Platform which is to be self-perpetually funded through DAOSYS, hence being its own bank. It will do this by lending its earned funds to build the ecosystem, and increasing inherent value in a virtuous cycle of utility. We understand that specific business models may become irrelevant over time as companies organically typically grow and die over time based on the inability to adapt its business practices and revenue models to the existing market trends, however the DAO model we have created is agnostic of revenue models and is completely driven by decentralized principles and tokenomics which are flexible to build value in the best way possible, maximizing the value of entire ecosystem with the minimal social and financial overhead costs. All of our products will be based on user acquisition, open source and extracting maximal value into the appreciation of the ecosystem.

### Network Enhanced Virtual Machine

In Dec 2021, Syscoin released the first stage of its Network Enhanced Virtual Machine (NEVM) which utilizes the Ethereum Virtual Machine (EVM). In the coming months (from the time of this publication), this will include a Zero Knowledge Proof (ZKP) system to build layer 2 (L2) scalable applications \[13], \[14], and one of the first of these applications will be DAOSYS.

### Usecases

#### Masternode Yield Farming

Yield farming is a technique that uses DeFi to maximize returns where investors submit liquidity to a decentralized application (ie, dApp) to earn yield on their principle using various methods. These methods are classified into four main types which include: staking, lending, borrowing, and utilizing liquidity providers, which is largely done on a decentralized exchange (DEX).

Syscoin plans to incentivize Masternode operators where they can put yields to work by investing them into a DeFi liquidity provider which will be automated in a trustless manner through DAOSYS. Hence, extending the Syscoin ecosystem, and increasing daily volumes. This system of trustlessly investing Masternode yields into a DeFi liquidity provider is what we call Masternode Yield Farming, which will serve as the first intended usecase for DAOSYS and will be the first of its kind in the crypto space.

Currently, there are approximately 2,500 Masternodes running on the Syscoin network. In \[7], we ran a case study with a five-year projection analysis on an additional 400 Mastern- odes, while at the same time factoring in network growth. We applied all these components into our model to estimate daily supply growth of the network, along with its respective confidence intervals; see Appendix B for details. With this tokenomics model, we estimated the expected share a typical node contributes to the network on a daily basis. Finally, with expected share, we estimated the five-year output of 400 new Masternodes; see Table 2 for details.

Overall, we are predicting an overall return of 14.7M SYS which represents a five-year return of 36.8% from the original investment of 40M SYS; see Fig. 7. Without DAOSYS, we would only realize an overall return of 31.2%. Keep in mind that the principle investment of 100K SYS is not subject to risk as the estimated DAOSYS returns are utilizing Masternode returns as its principle.

<figure><img src="../.gitbook/assets/supply_tot_reward_output.png" alt=""><figcaption><p>FIGURE 7: Predicted five-year returns from 400 new Syscoin masternodes starting Jan 2023, which include both net posi- tive yields from both Masternode and DAOSYS; (TOP) daily returns; and (BOTTOM) cumulative returns.</p></figcaption></figure>

The Syscoin Foundation will allocate $20M SYS into SYS Labs. At an estimated $27M USD peak valuation for 2023, SYS Labs will execute the master node yield strategy using its rewards. This will enable liquidity events which investors of SYS Labs can execute on through token warrants in exchange for equity. Masternode ROI will be used to deposit into DAOSYS which will be used to fund ecosystem initiatives as well as pay out token warrants to SYS Labs investors looking to exit. Analysis on Masternode ROI based on price modelling through to year 2028; see \[9] for Jupyter notebook. Analysis on DAOSYS ROI based on price modelling through to year 2025 (not including value created through lending to builders to build ecosystem objectives); see \[9].

The same yield strategy (executed through DAOSYS) will also be executed to any of our own tokens we create through DeFi cloning protocols or tokens we create through our innovations (e.g., rollup gas tokens, wallet token, LUXY, ZKCross, etc.) where applicable. Token warrants would be issued and executed on via DAOSYS using an exit mechanism similar to the Masternode Yield Strategy. Also, the act of using DAOSYS to create an exit vehicle helps the remaining investors in the strategy by creating liquidity events that promote the growth of the DAO itself as well as the ecosystem. This is a form of vesting that matures over time. Thus giving unlimited upside potential at the expense of time value while maximizing positive effect of liquidity events instead of being parasitic to the rest of the investors.

| Date | USD    | USD (lwr) | USD (upr) | # nodes  |
| ---- | ------ | --------- | --------- | -------- |
| 2023 | $78K   | $51K      | $166K     | 400/3044 |
| 2024 | $251K  | $76K      | $465K     | 400/3123 |
| 2025 | $932K  | $215K     | $1.54M    | 400/3198 |
| 2026 | $2.41M | $534K     | $3.32M    | 400/3270 |
| 2027 | $5.24M | $734K     | $7.27M    | 400/3338 |

#### Index Tokens (Crypto ETFs)

While the concept of indexing in the equity market is well established, it is surprising to see that this principle has yet to be largely applied to the crypto market using smart contracts. Hence, since DAOSYS itself is a non-speculated asset backed index of cryptos, for the first time we introduce a new class of cryptos called index tokens or crypto ETFs. The intelligence of the DAOSYS protocol will allow for the seamless, secure deployment of these index tokens using one of its readily available templates addressing this important usecase.

To put into perspective, under John Boogle’s direction, Vanguard is credited with the creation of the first index fund which was made available to the individual investor \[10]. This index fund was created in 1957, and was passively tied to the performance of the S\&P 500. Boogle is known as the founder of The Vanguard Group, which as of today (ie, Sept 2022), manages $7 trillion in assets. When investing long- term, Boogle argues the most efficient way to invest, is to simply buy the market itself, and that over time when looking at funds as a whole, they as a collective always revert to the mean. He also argues that over time, actively managed funds underperform the market, no matter what the current performance is.

Given the high volatility in the crypto market, and the fact that projects are continually entering and exiting the top 100 or even top 10 projects at a much higher frequency, we propose to simplify this problem and limit our attention to the top two crypos being BTC and ETH, with the introduction of what we term Bithereum. In Fig. 8 we see the advantage of developing an index token using this simple and effective strategy as we compare Bitcoin performance against the performance of various weighting strategies with Ethereum. Also, from a point of reasoning, it makes good sense to create an index token with BTC and ETH for the following reasons:

* ETH and BTC have been the top two projects by market cap for the past 5 years
* ETH is a good proxy for the altcoin market which perform better in bull markets, while BTC is a good proxy for crypto gold which perform better in bear markets
* The combined market cap share of the crypto space of both of these two projects has fluctuated between 60-90%
* Market cap share between ETH and BTC is negatively correlated against each other (p-val ∼ 0)
* ETH encapsulates large portions of other sectors (DeFi, NFT, etc) of the crypto space

<figure><img src="../.gitbook/assets/index_coin.png" alt=""><figcaption><p>FIGURE 8: Comparison of various Bithereum index coin market weighting strategies beginning at the 2020 BTC hal- vening with $1 initial investment. We see that compared to just BTC alone, that a 50/50 weighting of BTC and ETH would outperform BTC by approximately 16 times.</p></figcaption></figure>

It is surprising that with all the developments that have happened in crypto, and given the success that ETFs have had in traditional finance, we have not yet seen adoption of this idea into crypto yet. However, DAOSYS with its smart DAO features will allow for the secure and seamless deployment of these new class of cryptos.

### Launch Expectations

Prior to mainnnet release, Syscoin’s L2 (ie, Rollux) \[12]– \[14] must launch first along with Syscoin’s Proof-of-Data Availability (PoDA) \[11]. While it is technically possible that DAOSYS can run from any layer 1 (L1) EVM blockchain, it is our intention that it be launched when Rollux goes live. Currently, DAOSYS is running on the Rollux testnet where it is also running a test DAO for Pegasys, which is Syscoin’s premiere decentralized exchange (DEX).

We are expecting to launch DAOSYS in the early part of 2023 with crypto’s first Masternode Yield Farm as its first functioning child DAO; see Fig. 9. Hence other projects running Masternodes will be incentivized to use our template and join the ecosystem to earn additional yield following the business case outlined in Section VI-C1.

<figure><img src="../.gitbook/assets/daosys_launch.png" alt=""><figcaption><p>FIGURE 9: DAOSYS expected ecosystem at launch in early 2023</p></figcaption></figure>
