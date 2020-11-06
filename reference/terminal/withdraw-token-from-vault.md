# withdraw-token-from-vault

Withdraw tokens 

# usage

```sh
withdraw-token-from-vault <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following
  
    - `USDT`
    - `WETH`
    - `WBTC`
    
- `[AMOUNT]` (optional): default value is all of the balance of account

# examples

- burn `100` `fWBTC` to withdraw `WBTC`

    ```sh
    withdraw-token-from-vault WBTC 100 
    ```

- burn all `fUSDT` to withdraw `USDT`

    ```sh
    withdraw-token-from-vault USDT 
    ```