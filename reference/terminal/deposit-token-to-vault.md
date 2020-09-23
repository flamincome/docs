# connect-wallet

connect metamask wallet

# usage

```sh
deposit-token-to-vault <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following
    
    - `USDT`
    - `TUSD`
    - `USDC`
    - `DAI`
    - `WETH`
    - `WBTC`
    - `sBTC`
    - `renBTC`

- `[AMOUNT]` (optional): default value is all of the balance of account

# examples

- deposit `100` `WBTC` to mint `fWBTC`

    ```sh
    deposit-token-to-vault WBTC 100 
    ```

- deposit all `USDT` to mint `fUSDT`

    ```sh
    deposit-token-to-vault USDT 
    ```