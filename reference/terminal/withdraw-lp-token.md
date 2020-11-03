# withdraw-lp-token

withdraw liquidity token

# usage

```sh
withdraw-lp-token <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following
  
    - `UNI-V2[USDT]`
    - `UNI-V2[WETH]`
    - `UNI-V2[WBTC]`
    
- `[AMOUNT]` : The amount of liquidity tokens to withdraw

# examples

- withdraw `100` `UNI-V2[WBTC]` liquidity token

    ```sh
    withdraw-lp-token UNI-V2[WBTC] 0.01 
    ```

    
