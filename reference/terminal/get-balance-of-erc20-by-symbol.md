# get-balance-of-erc20-by-symbol

get erc20 balance

must connect-wallet first

# usage

```sh
get-balance-of-erc20-by-symbol <TOKEN_SYMBOL> [address]
```

- `<TOKEN_SYMBOL>`: can be one of the following
    - `USDT`
    - `WETH`
    - `WBTC`
    
- `[address]`(optional): the address of wallet; default value is the connected wallet

# examples

- get erc20 balance of `USDT`

    ```sh
    get-balance-of-erc20-by-symbol USDT 
    ```

- get erc20 balance of `USDT `of someone's wallet

    ```sh
    get-balance-of-erc20-by-symbol USDT 0x8e2d8a70D747a4b1979BDA39aE6b3260F77b0e23(this is an invalid address,for reference only )
    ```

