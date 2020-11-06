# FlamIncome Terminal

[FlamIncome Terminal](https://flamincome.finance) provides a terminal UI for professional users.

Use [FlamIncome Web App](https://app.flamincome.finance/) or [Income Page of Flamingo](https://flamingo.finance/income) if you feel the terminal UI is not easy to use.

# Guide

Users can enter commands in FlamIncome Terminal UI for operations.

For more info about the commands, please check out [FlamIncome Terminal Reference](https://docs.flamincome.finance/reference/terminal)

###### Procedures for providing liquidity and obtaining rewards:

Using USDT as an example:

1. Use [`Deposit Token to FlamIncome`](#deposit) command to deposit a portion of USDT into vault and receive fUSDT (You must keep a part of your USDT tokens for providing liquidity in the following step)
2. Use [`Deposit fToken to Mint nToken`](#fton) command to convert the fUSDT that you get from the previous step to nUSDT
3. Provide liquidity in Uniswap using the newly minted nUSDT and the remaining USDT you hold. The corresponding Uniswap liquidity pool address is listed in [`Provide Liquidity in Uniswap`](#uni) section 
4. After successfully providing liquidity in Uniswap, you can use [`Stake LP Tokens`](#stake) to stake the LP tokens received from Uniswap into the staking pools
5. After staking the LP tokens for a period of time, users can find out the amount of FLAG token rewards they can get via using the [`Get Staking Earning`](#earning) operation
6. Users can also check the number of LP Tokens they staked by using [`Get Staking Amount`](#stakingamount) command
7. Lastly, users can use [`Claim Staking Rewards`](#claim) for withdrawing FLAG rewards they obtained through staking LP tokens

###### Procedures for withdrawing LP tokens and removing liquidity:

Again, taking USDT as example:

1. First, users need to withdraw LP tokens by following the [`Withdraw LP Tokens`](#withdraw) step. After withdrawing all the LP tokens users will no longer be able to receive FLAG rewards
2. After getting back LP tokens, users can remove liquidity from Uniswap. The liquidity pools address are provided in [`Remove Liquidity in Uniswap`](#removel)
3. Users will receive nUSDT after removing liquidity in Uniswap and can follow the [`Convert nToken to fToken`](#ntof) procedure to convert nUSDT to fUSDT, which can be used to withdraw tokens from FlamIncome
4. Final step, if users want to withdraw certain amount of USDT, they can use [`Withdraw Token from FlamIncome`](#withdrawToken) to perform this operation

** Note: The next section detailedly explained the syntax and usage of each command in the highlighted portions

## <a name="deposit">Deposit Token to FlamIncome</a>

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
   - `WETH`
   - `WBTC`
   
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

## <a name="withdrawToken">Withdraw Token from FlamIncome</a>

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
   - `WETH`
   - `WBTC`
   
   `[AMOUNT]` (optional): default value is the current balance of account
   
3. Example

    Withdraw 1000 USDT

    ```sh
    withdraw-token-from-vault USDT 1000
    ```

## <a name="fton">Deposit fToken to Mint nToken</a>

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
   - `WETH`
   - `WBTC`
   
   `DEPOSIT`: the amount of fTokens you want to deposit
   
   `MINT`: the amount of nTokens you want to get 
   
** It is recommended that you enter the same amount for deposit and mint.
   
3. Example

   Deposit 100 `fUSDT` and get 100 `nUSDT` 

   ```
   deposit-ftoken-to-normalizer USDT 100 100
   ```

## <a name="uni">Provide Liquidity in Uniswap</a>

You can provide liquidity in three Uniswap pools: 

* [nUSDT-USDT](https://app.uniswap.org/#/add/0x2205d2f559ef91580090011aa4e0ef68ec33da44/0xdac17f958d2ee523a2206206994597c13d831ec7)

* [nWETH-WETH](https://app.uniswap.org/#/add/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xe179198fd42f5de1a04ffd9a36d6dc428ceb13f7)

* [nWBTC-WBTC]( https://app.uniswap.org/#/add/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xbb44b36e588445d7da61a1e2e426664d03d40888)

Make sure that you have sufficient amount of tokens in your account before providing liquidity.

## <a name="stake">Stake LP Tokens</a>

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

   `[AMOUNT]`(optional) : The amount of tokens to stake, the default value is the current balance of LP tokens

3. Example

   Stake `0.01 ` `WBTC` liquidity token into corresponding pool

   ```sh
   stake-lptoken WBTC 0.01 
   ```


## <a name="claim">Claim Staking Rewards</a>

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

## <a name="stakingamount">Get Staking Amount</a>

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

## <a name="earning">Get Staking Earning</a>

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

## <a name="withdraw">Withdraw LP Tokens</a>

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

   `AMOUNT`: the amount of LP Tokens to withdraw, the default value is the current balance of LP tokens

3. Example

   Withdraw 0.01`WBTC` LP token from corresponding pool

   ```sh
   unstake-lptoken WBTC 0.01 
   ```

## <a name="removel"> Remove Liquidity in Uniswap</a>

You can remove liquidity from three Uniswap pools: 

* [nUSDT-USDT](https://app.uniswap.org/#/remove/0x2205d2f559ef91580090011aa4e0ef68ec33da44/0xdac17f958d2ee523a2206206994597c13d831ec7)

* [nWETH-WETH](https://app.uniswap.org/#/remove/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xe179198fd42f5de1a04ffd9a36d6dc428ceb13f7)

* [nWBTC-WBTC]( https://app.uniswap.org/#/remove/0x2260fac5e5542a773aa44fbcfedf7c193bc2c599/0xbb44b36e588445d7da61a1e2e426664d03d40888)

## <a name="ntof">Convert nToken to fToken</a>

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
   - `WETH`
   - `WBTC`
   
3. Example

   Burn all ntoken of `USDT` to withdraw ftoken

   ```
   withdrawall-ftoken-from-normalizer USDT 
   ```

