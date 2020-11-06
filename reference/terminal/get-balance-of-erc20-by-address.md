# get-balance-of-erc20-by-address

get erc20 balance

must connect-wallet first

# usage

```sh
get-balance-of-erc20-by-address <TOKEN_ADDRESS> [address]
```

- `<TOKEN_ADDRESS>`: can be one of the following
    - The address of one token can be found by using `list-registry-of` command
    
- `[address]`(optional): the address of wallet; default value is the connected wallet

# examples

- get erc20 balance of `USDT`(`0xdAC17F958D2ee523a2206206994597C13D831ec7`)

    ```sh
    get-balance-of-erc20-by-address 0xdAC17F958D2ee523a2206206994597C13D831ec7 
    ```

- get erc20 balance of `USDT` of someone's metamask

    ```sh
    get-balance-of-erc20-by-address 0xdAC17F958D2ee523a2206206994597C13D831ec7(the add of USDT) 0x8e2d8a70D747a4b1979BDA39aE6b3260F77b0e23(this is an invalid address,for reference only )
    ```

