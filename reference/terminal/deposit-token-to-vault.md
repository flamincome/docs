# deposit-token-to-vault 

Deposit a portion of USDT into vault and receive fUSDT 

# Usage

```sh
deposit-token-to-vault <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following
  
    - `USDT`
    - `WETH`
    - `WBTC`
    
- `[AMOUNT]` (optional): default value is all of the balance of account

# Examples

- deposit `100` `WBTC` to mint `fWBTC`

    ```sh
    deposit-token-to-vault WBTC 100 
    ```

- deposit all `USDT` to mint `fUSDT`

    ```sh
    deposit-token-to-vault USDT 
    ```
