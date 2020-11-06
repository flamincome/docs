# stake-lptoken

* stake liquidity token

# Usage

```sh
stake-lptoken <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be any of the following
  - `USDT`
  - `WETH`
  - `WBTC`

- `[AMOUNT]` (optional) : The amount of tokens to stake, the default value is the current balance of LP tokens

# Example

- stake `0.01` `WBTC` liquidity token into the corresponding pool

    ```sh
    stake-lptoken WBTC 0.01 
    ```

    
