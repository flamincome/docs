# get-apy-of-ftoken-by-symbol

get apy of a vault

must connect-wallet first

# usage

```sh
get-apy-of-ftoken-by-symbol <TOKEN_SYMBOL> [amount]
```

- `<TOKEN_SYMBOL>`: can be one of the following
    - `USDT`
    - `WETH`
    - `WBTC`
    
- `[amount]`(optional): the amounts of blocks; default value is `10000`

# examples

- get apy of a vault of `USD`

    ```sh
    get-apy-of-ftoken-by-symbol USDT 
    ```

- get apy of a vault of `USDT`  of 1000 blocks

    ```sh
    get-apy-of-ftoken-by-symbol USDT 1000
    ```

