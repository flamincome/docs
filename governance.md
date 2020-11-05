# FlamIncome Governance

> FlamIncome was launched in September 2020, and the peak of its TVL (Total Value Locked) is currently over 0.7 billion USD. Flamincome Governance was originally managed by a [multi-sig wallet](https://etherscan.io/address/0x9832a79C563d31ether403409C41f92C51b824435cdB0), which is replaced by a fully decentrilized DAO in October 2020.

The governance of FlamIncome is based on [Aragon](https://aragon.org).

`FLAG` is the governance token of FlamIncome.

# FlamIncome Governance Token

> **All the governance mechanism can be changed by the governance mechanism itself**

The FlamIncome Governance Token is `FLAG`, and its initial supply in the first year is `1,048,576 FLAG`.

Starting from the second year, additional tokens which equals to `100%` of the original supply will be distributed each year. The total supply in the second and third year will be `2,097,152 FLAG` and  `4,194,304 FLAG`,respectively. 

`50%` of the tokens (including the initial supply in the first year) will be awarded to liquidity providers staking in `USDT-nUSDT`, `WBTC-nWBTC`, and `WETH-nWETH` liquidity pools. The `50%` of staking rewards tokens will be distributed to `USDT-nUSDT` pairs, `25%` to `WBTC-nWBTC` pairs, and `25%` to `WETH-nWETH` pairs.  

The remaining `50%` of the tokens (including the initial supply in the first year) will be distributed to users who participate in the governance (voters).

The purpose of the high inflation rate is to give continuous incentives to new contributors. In another words, if one currently holds `1` `FLAG`, the only way to maintain its token's value (anti-inflation) is to provide liquidity continuously or vote in the DAO.

## Staking Rewards
Stake LP (liquidity provider) tokens to mint FLAG. 
Currently we support `3` LP tokens in Uniswap (`USDT-nUSDT`, `WBTC-nWBTC`, `WETH-nWETH`) to stake and earn FLAG. FLAG will be allocated to individuals based on their staking duration and proportional to the amount of LP tokens they own in the pools.

## Voting Rewards
This is an incentive plan for encouraging active participations in the governance of the community.
Voting rewards are calculated based on the equation below:

```
gapi = startDatei - startDatei-1 
rewardsi = stake/(yeai+nayi) * gapi/oneYear * totalSupply
rewards = ∑rewardsi
```

`i` : the ith governance proposal

`gapi`: the time interval between the starting time of this vote and the starting time of the previous vote

`yeai+nayi`: the sum of those who voted yes and no.

`oneYear`: the total time for governance vote awards is oneYear.

`totalSupply`: the total number of governance votes awarded, namely 524,288

This equation allows users to calculate the number of tokens they can obtain in a proposal vote.

If the user participates in more than one vote, the `rewards` will equal to the sum of the rewards for each vote.

The community's first vote will be on token allocation to the Flamincome project team. One can choose YES/NO in the poll to decide whether or not to ditribute FLAG tokens to the team. Initially the vote will decide if the team can get `6.25%` additional FLAG tokens. Once the issue is approved, the amount will increase by `6.25%` each time until the community rejects the proposal. 

# FlamIncome Improvement Proposal

FlamIncome provides strong proposals and weak proposals.

Strong proposals will execute immediately after the close of the polling.

Weak proposals don't make any actual changes, but they represent the opinions of the community on certain issues.

## Strong Proposal

Proposals such as minting `FLAG` tokens or proposing new strategies are considered as strong proposals. Strong proposals will be executed immediately after voting. No one can stop an approved strong proposal, not even the FlamIncome team.

## Weak Proposal

Proposals for the purpose of expressing opinions and views in the community will not result in any executions on smart contract, thus weak proposals don't make any actual changes.

