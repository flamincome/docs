# add-liquidity

add liquidity in Uniswap and get lp tokens

# usage

```sh
add-liquidity <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following
  
    - `USDT`
    - `WETH`
    - `WBTC`
    
- `[AMOUNT]` : The amount of tokens to add liquidity

# examples

- add liquidity to `WBTC- nWBTC` pairs with 100 WBTC (corresponding nWBTC will be calculated by Uniswap)

    ```sh
    add-liquidity WBTC 100 
    ```

    
