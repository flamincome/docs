# FlamIncome Governance

> FlamIncome is launched in September of 2020 and its peak TVL reached more than 0.7 billion dollars.
> Governance of Flamincome is managed by a [multi-sig wallet](https://etherscan.io/address/0x9832a79C563d31ether403409C41f92C51b824435cdB0) at first, and it is replaced by a fully decentrilized DAO in October of 2020.

Governance of FlamIncome is based on [Aragon](https://aragon.org).

`FLAG` is the governance token of FlamIncome.

# FlamIncome Governance Token

> **All the governance mechanism can be changed by the governance mechanism itself**

The symbol of FlamIncome Governance Token is `FLAG` and its total supply in the first year is `1048576`.

Since the second year, `FLAG` inflation rate will be `100%` per year, which means, total suply is `2097152` in the second year, total supply is `4194304` in the third year ...

`50%` of the infalted tokens (including the inital supply in the first year) will be distributed to the liquidity provider between `nXXX` tokens (i.e. `nUSDT`) and original `XXX` (i.e. `USDT`) tokens.

The other `50%` of the infalted tokens (including the inital supply in the first year) will be distributed to users who participate in the governance (voters).

The high inflation rate is for continuously incentive the new contributors, in another word, if one hold `1` `FLAG`, the only way to keep its token weight (anti-inflation) is to provide liquidity continuously or vote in the DAO.

## Staking Rewards
Stake LP(liquidity provider) tokens to mint FLAG. 
Now we support `6` LP tokens from Uniswap(`nwbtc/wbtc`, `nweth/weth`, `nusdt/usdt`) and Curve (`nwbtc/wbtc`, `nweth/weth`, `nusdt/usdt`)  to stake and get FLAG. 6 pools will share the rewards equally(i.e. `0.33^20`/pool for first year). The rewards will be calculated by year for our FLAG distribution strategy. FLAG will be allocated to who has staked proportional to the total time and the ratio of individual LP tokens to totalsupply.

## Voting Rewards
This is an Incentive plan to encourage everyone to participate in the governance of community.
Voting rewards are calculated based on the equation below:
$$
gap_{i}=startDate_{i}-startDate_{i-1}   \\
rewards_{i}=\frac{stake}{yea_{i}+nay_{i}}*\frac{gap_{i}}{oneYear}*totalSupply\\
rewards=\sum rewards_{i}
$$

In the equation, `i` means that you are the `ith` person voting. `gapi` is the total time from the last vote to now. if `i` equals 1, `startDate0` means the start time of this vote. `stake` is the LP tokens one has staked. `yeai` and `nayi` are referred to the sum of concurring and dissenting vote when voting.

The community's first vote will be on the inflation of token allocation to the Flamincome project team. When voting one can choose YES/NO to decide whether to increase the team FLAG by `5%` every time.

# FlamIncome Improvement Proposal

There are strong proposals and weak proposals in FlamIncome.

Strong proposals will executed once it is allowed by the DAO.

Weak proposals don't make any actual changes, but it is the opinion of the community on some principles.

## Strong Proposal

To propose a strong proposal, like minting `FLAG` tokens to distribute to someone, or propose a new strategy. These kind of proposals will be regarded as strong proposal, which will be executed immediately once approved by voting, therefore no one can stop an approved strong proposal, including the Flamincome team.

## Weak Proposal

To propose a weak proposal, like expressing someone's opinions and views in the community, which will not result in any execution on smart contract, thus weak proposals don't make any actual changes.

