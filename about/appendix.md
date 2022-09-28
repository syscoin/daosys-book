# Appendix

### Appendix A: EIP-2535 (DIAMOND FACETS)

EIP-2535 was an Ethereum proposal launched in 2020 to allow for the creation of modular contract systems that can be extended after deployment \[5]. To solve this problem, this new proposal introduced a concept known as Diamonds. A Diamond refers to a smart contract system where functionality and storage is split up into separate contracts, and is an extension of a proxy contract.

A proxy contract is the the immutable part a user interacts with which holds data. It contains a fallback function which will catch any function call and use `delegatecall` to forward it to a second logic contract. A `delegatecall` will execute a function defined in the called contract (logic), but within the context of the calling contract (proxy). Thus, we have our logic defined separately from our data. This allows users to change the logic contract without changing the immutable underlying data.&#x20;

There are several limitations to proxy contracts which include: (a) implementing minor upgrades; (b) 24kb max con- tract size limit; (c) can only create identical proxy instances using one logic contract; and (d) cannot have a modular permission system. Diamonds solve these issues by allowing for multiple logic contracts which talks to the original proxy contract via the `delegatecall`; for comparison between these two systems see Fig. 10 .

<figure><img src="../.gitbook/assets/diamonds.png" alt=""><figcaption><p>FIGURE 10: Multi-facet proxy; (TOP) prior to EIP-2535, proxy contracts could only make delegates calls to another contract only; (BOTTOM) EIP-2535 introduced the capability of performing delegates calls to multiple contracts</p></figcaption></figure>

### Appendix B: Masternode Tokenomics Model

The Masternode Yield Farming tokenomics model has two main components: (a) Masternode rewards; and (b) DAOSYS rewards. To acquire Masternode rewards, users stake liquidity to purchase a Masternode, thus used to generate $$Coins_{New}$$in accordance to the specifications described in \[14], which are as follows:

* **Block time**: 150 seconds
* **Halving interval**: 210240 (1 year)
* **Base Rewards**: 96.25 SYS per block deflated 5 percent every 210240 blocks
* **NEVM Rewards**: 10.55 SYS per block (not deflated) EIP1559 model
* **Governance Proposals**: 10 percent of Base Rewards paid out every 17520 blocks (1 month)
* **Miner/Masternode Subsidy**: 90 percent of Base Re- wards. 25 percent of this value goes to miner, 75 percent of this value goes to Masternode
*   **Masternode Minimum Subsidy**: 5.275 SYS (can not

    go below this amount even accounting for deflation)
* **Masternode collateral requirement**: 100,000 SYS
*   **Masternode seniority**: 35 percent increase after

    210240 blocks (1 year), 100 percent increase after 525600 blocks (2.5 years)

Using the rule set described above, we determine Masternode rewards via the following:

$$
MN_{Rewards} = (Blocks_{Num}) (Coins_{New}) \left(\frac{Nodes_{Num}}{Supply_{Cur}}\right),
$$

where current supply is calculated via the following:

$$
Supply_{Cur} = Supply_{Prev} + Coins_{New} - Fee_{TXBurn},
$$

​and $$Fee_{TXBurn}$$ is calculated in accordance to the section below. Finally, total rewards were determined via the following:

$$
Total_{Rewards} = MN_{Rewards} + DAOSYS_{Rewards}.
$$

To estimate $$DAOSYS_{Rewards}$$ we used our DeFi python simulator; for tutorials and example templates one can reference \[8]. To estimate returns in USD, we applied the Monte Carlo procedure to estimate future point predictions for the USD value of Syscoin, as per section below.

#### Transaction Fee Burn

To model transaction fee burn to determine the supply end we used Ethereum fee data to serve as a proxy. We have de- termined that transaction fees follow an exponential growth that can be modelled via the following log-log model:

$$
ln(\hat{y_{t}}) = a + bln(x_{t}),
$$

​where parameters $$a$$ and $$b$$ and its confidence intervals can be estimated using Ordinary Least Squares (OLS).

#### Price Point Predictions: Monte Carlo

To generate point predictions for the price of Syscoin, we made some assumptions. Price was given the freedom to fluctuate between $0.25 to $25 USD / SYS over the five-year projection interval (ie, 2023-2028) while maintaining an overall upward logarithmic growth, which is a price behavior characteristic that can be attributed to most successful crypto projects. To do this we generated a set of Monte Carlo point predictions, $$\mathbf{\hat{p}}_{t}$$, using the following:

$$
\mathbf{\hat{p}}_{t} = c + \mathbf{\tilde{z}}_{t}e^{k z_{t}},
$$

​where random drift term $$\mathbf{\tilde{z}}_{t}$$is normalized between \[$$a_{lwr},b_{upr}$$] as given by:

$$
\mathbf{\tilde{z}}_{t}= \frac{\mathbf{z}_{t} - min(\mathbf{z}_{t})}{max(\mathbf{z}_{t}) - min(\mathbf{z}_{t})},
$$

​and $$\mathbf{z}_{t}$$is an ARIMA(1,1,1) process, given by:

$$
\mathbf{z}_{t} = \gamma + \mathbf{z}_{t-1} + \phi_{1} \mathbf{z}_{t-1} - \phi_{1} \mathbf{z}_{t-2} +  \theta_{1} \mathbf{e}_{r-1} + \mathbf{e}_{t},
$$

​where $$\phi_{1}$$is the AR(1) coefficient, $$\theta_{1}$$is the MA(1) coefficient, and $$\mathbf{e}_{t} \sim N(0, \sigma^2)$$. Once these sets were generated, we estimated the $$5^{th}$$ and $$95^{th}$$percentiles to attain the 90% prediction interval. For a table of these point predictions along with its corresponding confidence interval, see \[8].
