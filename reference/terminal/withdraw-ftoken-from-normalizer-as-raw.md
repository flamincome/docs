# withdraw-ftoken-from-normalizer-as-raw

burn ntoken to withdraw ftoken

must connect wallet first

# usage

```sh
withdraw-ftoken-from-normalizer-as-raw <TOKEN_SYMBOL> [left] [right]
```

- `<TOKEN_SYMBOL>`: can be one of the following
  
    - `USDT`
    
    - `WBTC`
    
    - `WETH`
    
       there is no default value, you must enter argument
    
- `[left]`: 

- `[right]`: 

# examples

- burn ntoken of `USDT` to withdraw ftoken range from `10` to `50`

    ```sh
    withdraw-ftoken-from-normalizer-as-raw USDT 10 50
    ```