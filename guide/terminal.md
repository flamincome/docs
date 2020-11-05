# FlamIncome Terminal

[FlamIncome Terminal](https://flamincome.finance) provides a terminal UI for professional users.

Use [FlamIncome Web App](https://app.flamincome.finance/) or [Income Page of Flamingo](https://flamingo.finance/income) if you feel the terminal UI is not easy to use.

# Guide

Users can enter commands in FlamIncome Terminal UI for operations.

For more info about the commands, please check out [FlamIncome Terminal Reference](https://docs.flamincome.finance/reference/terminal)

## Deposit Token to FlamIncome

1. Connect to wallet

   ```sh
   connect-wallet
   ```

2. Deposit tokens 

   ```sh
   deposit-token-to-vault <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   - `USDT`
   - `TUSD`
   - `USDC`
   - `DAI`
   - `WETH`
   - `WBTC`
   - `sBTC`
   - `renBTC`

   `[AMOUNT]` (optional): default value is the current balance of account

3. Example

   Deposit `1000` `USDT`

   ```sh
   deposit-token-to-vault USDT 1000
   ```

   (optional): Enter the following command to see the address of flamincome token and add it to metamask (click the `Add Token` button on the `Assets`, then click on  `Custom Token` and paste the address into `Token Contract Address`)

   ```sh
   list-registry-of-vaults
   ```

   (optional): Enter the following command to see your flamincome token balance

   ```sh
   get-balance-of-ftoken-by-symbol USDT
   ```

## Withdraw Token from FlamIncome

1. Connect to wallet

    ```sh
    connect-wallet
    ```

2. Withdraw tokens 

   ```sh
   withdraw-token-from-vault <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   - `USDT`
   - `TUSD`
   - `USDC`
   - `DAI`
   - `WETH`
   - `WBTC`
   - `sBTC`
   - `renBTC`

   `[AMOUNT]` (optional): default value is the current balance of account

3. Example

    Withdraw 1000 USDT

    ```sh
    withdraw-token-from-vault USDT 1000
    ```

## Deposit fToken to Mint nToken

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Deposit ftoken to mint ntoken

   ```sh
   deposit-ftoken-to-normalizer <TOKEN_SYMBOL> [DEPOSIT] [MINT]
   ```

   Note: `TOKEN_SYMBOL` has no default value, thus you must enter an argument

   `<TOKEN_SYMBOL>`: can be any of the following

   - `USDT`
   - `TUSD`
   - `USDC`
   - `DAI`
   - `WETH`
   - `WBTC`
   - `sBTC`
   - `renBTC`

   `DEPOSIT`: the amount of fTokens you want to deposit

   `MINT`: the amount of nTokens you want to get 

   ** It is recommended that you enter the same amount for deposit and mint.

3. Example

   Deposit 100 `fUSDT` and get 100 `nUSDT` 

   ```
   deposit-ftoken-to-normalizer USDT 100 100
   ```

## Provide Liquidity in Uniswap

You can provide liquidity in three Uniswap pools: 

* [nUSDT-USDT](https://app.uniswap.org/#/add/0x2205d2f559ef91580090011aa4e0ef68ec33da44/0xdac17f958d2ee523a2206206994597c13d831ec7)

* [nWETH-WETH](https://app.uniswap.org/#/add/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xe179198fd42f5de1a04ffd9a36d6dc428ceb13f7)

* [nWBTC-WBTC]( https://app.uniswap.org/#/add/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xbb44b36e588445d7da61a1e2e426664d03d40888)

Make sure that you have sufficient amount of tokens in your account before providing liquidity.

## Stake LP Tokens

Stake LP tokens and get FLAG tokens as reward

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Stake liquidity tokens

   ```sh
   stake-lptoken <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

   `[AMOUNT]`(optional) : The amount of tokens to stake, default value is the current balance of LP token.

3. Example

   Stake `0.01 ` `WBTC` liquidity token into corresponding pool

   ```sh
   stake-lptoken WBTC 0.01 
   ```


## Claim Staking Rewards

Get FLAG token rewards earned through staking LP tokens

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Claim staking rewards

   ```sh
   claim-reward-of-staking <TOKEN_SYMBOL>
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

3. Example

   Claim staking reward in WBTC account

   ```sh
   claim-reward-of-staking WBTC
   ```

## Get Staking Amount

Check the current amount of LP tokens that the user have

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Check the amount of tokens in the account 

   ```sh
   get-amount-of-staking <TOKEN_SYMBOL>
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

3. Example

   Check the amount of staked WBTC LP tokens

   ```sh
   get-amount-of-staking WBTC
   ```

## Get Staking Earning

Query the amount of FLAG rewards obtained by the user

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Query staking rewards obtained via staking LP tokens

   ```sh
   get-earning-of-staking <TOKEN_SYMBOL>
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

3. Example

   Check how many FLAG tokens you earn from staking WBTC LP tokens

   ```sh
   get-earning-of-staking WBTC
   ```

   ** Note: this command is only used to display the amount of rewards obtained by the user. Use `claim-reward-of-staking` for actually claiming the reward. 

## Withdraw LP Tokens

Withdraw LP Tokens from the account. Please note that user will no longer able to receive FLAG rewards after withdrawing the LP tokens. 

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Unstake the LP Tokens 

   ```sh
   unstake-lptoken <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

   `AMOUNT`: the amount of LP Tokens to withdraw

3. Example

   Withdraw 0.01`WBTC` LP token from corresponding pool

   ```sh
   unstake-lp-token WBTC 0.01 
   ```

## Remove Liquidity in Uniswap 

You can remove liquidity from three Uniswap pools: 

* [nUSDT-USDT](https://app.uniswap.org/#/remove/0x2205d2f559ef91580090011aa4e0ef68ec33da44/0xdac17f958d2ee523a2206206994597c13d831ec7)

* [nWETH-WETH](https://app.uniswap.org/#/remove/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xe179198fd42f5de1a04ffd9a36d6dc428ceb13f7)

* [nWBTC-WBTC]( https://app.uniswap.org/#/remove/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xbb44b36e588445d7da61a1e2e426664d03d40888)

## Convert nToken to fToken

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Burn ntoken to withdraw ftoken

   ```sh
   withdrawall-ftoken-from-normalizer <TOKEN_SYMBOL> 
   ```

   Note: TOKEN_SYMBOL has no default value, thus you mush enter an argument

   `<TOKEN_SYMBOL>`: can be any of the following

   - `USDT`
   - `TUSD`
   - `USDC`
   - `DAI`
   - `WETH`
   - `WBTC`
   - `sBTC`
   - `renBTC`

3. Example

   Burn all ntoken of `USDT` to withdraw ftoken

   ```
   withdrawall-ftoken-from-normalizer USDT 
   ```

**Etherscan is also available for user to perform operations on staking LP tokens and receiving FLAG token rewards. The contract address are provided below:**

[USDT Contract Address](https://etherscan.io/address/0x5da42899d108FEF66689D46025ABB5E647B8477B#code)

[WETH Contract Address](https://etherscan.io/address/0xb9B1b40823e5B63d81794c6279AeBc3405B5534d#code)

[WBTC Contract Address](https://etherscan.io/address/0xBc85c2b7999D4fBeA71C30Bc3ba1Cac2A0648d9E#code)

