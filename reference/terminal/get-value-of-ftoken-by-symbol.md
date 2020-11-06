# get-value-of-ftoken-by-symbol

get underlying value of an account

must connect-wallet first

# usage

```sh
get-value-of-ftoken-by-symbol <TOKEN_SYMBOL> [address]
```

- `<TOKEN_SYMBOL>`: can be one of the following
    - `USDT`
    - `WBTC`
    - `WETH`
    
- `[address]`(optional): the address of wallet; default value is the connected wallet

# examples

- get underlying value of `USDT`

    ```sh
    get-value-of-ftoken-by-symbol USDT 
    ```

- get underlying value of `USDT` of someone's wallet

    ```sh
    get-value-of-ftoken-by-symbol USDT 0x8e2d8a70D747a4b1979BDA39aE6b3260F77b0e23(this is an invalid address,for reference only )
    ```

