# FlamIncome Terminal

[FlamIncome Terminal](https://flamincome.finance) provides a terminal UI for professional users.

Use [FlamIncome Web App](https://app.flamincome.finance/) or [Income Page of Flamingo](https://flamingo.finance/income) if you feel the terminal UI is not easy to use.

# Guide

Users can enter commands in FlamIncome Terminal UI for operations.

For more info about the commands, see [FlamIncome Terminal Reference](https://docs.flamincome.finance/reference/terminal)

## Deposit Token to FlamIncome

1. Connect to wallet

   ```sh
   connect-wallet
   ```

2. Withdraw tokens 

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

3. Example:

   Deposit `1000` `USDT`

   ```sh
   deposit-token-to-vault USDT 1000
   ```

   (optional): enter the following command to see the address of flamincome token and add it to metamask (click the `Add Token` button on the `Assets`, then click on  `Custom Token` and paste the address into `Token Contract Address`)

   ```sh
   list-registry-of-vault
   ```

   (optional): enter the following command to see your flamincome token balance

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

3. Example:

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

3. Example:

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

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Stake liquidity tokens

   ```sh
   stake-lp-token <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

   `[AMOUNT]` : The amount of tokens to stake

3. Example:

   Stake `0.01 ` `WBTC` liquidity token into corresponding pool

   ```sh
   stake-lp-token WBTC 0.01 
   ```


## Claim Staking Rewards

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

3. Example:

   Claim staking reward for WBTC account:

   ```sh
   claim-reward-of-staking WBTC
   ```

## Get Staking Amount

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Claim staking rewards

   ```sh
   get-amount-of-staking <TOKEN_SYMBOL>
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

3. Example:

   Check the amount of staking WBTC tokens:

   ```sh
   get-amount-of-staking WBTC
   ```

## Get Staking Earning

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Claim staking rewards

   ```sh
   get-earning-of-staking <TOKEN_SYMBOL>
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

3. Example:

   Check how much you earn from staking WBTC tokens:

   ```sh
   get-earning-of-staking WBTC
   ```

   ** Note: this command is only used to display the amount of rewards obtained by the user. Use `claim-reward-of-staking` for actually claiming the reward. 

## Withdraw LP Tokens

1. Connect to wallet

   ```sh
   connect-wallet 
   ```

2. Unstake the LP Tokens from Uniswap

   ```sh
   unstake-lptoken <TOKEN_SYMBOL> [AMOUNT]
   ```

   `<TOKEN_SYMBOL>`: can be any of the following

   * `USDT`

   * `WETH`

   * `WBTC`

   `AMOUNT`: the amount of LP Tokens to withdraw

3. Example:

   Withdraw 0.01`WBTC` liquidity token from corresponding pool

   ```sh
   unstake-lp-token WBTC 0.01 
   ```

## Remove Liquidity in Uniswap 

You can remove liquidity from three Uniswap pools: 

* [nUSDT-USDT](https://app.uniswap.org/#/add/0x2205d2f559ef91580090011aa4e0ef68ec33da44/0xdac17f958d2ee523a2206206994597c13d831ec7)

* [nWETH-WETH](https://app.uniswap.org/#/add/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xe179198fd42f5de1a04ffd9a36d6dc428ceb13f7)

* [nWBTC-WBTC]( https://app.uniswap.org/#/add/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xbb44b36e588445d7da61a1e2e426664d03d40888)

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

3. Example:

   Burn all ntoken of `USDT` to withdraw ftoken

   ```
   withdrawall-ftoken-from-normalizer USDT 
   ```