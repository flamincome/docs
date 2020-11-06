# list-registry-of-vaults

list registry of vaults

# usage

```sh
list-registry-of-vaults <TOKEN_SYMBOL> 
```

- `<TOKEN_SYMBOL>`(optional): can be one of the following
  
    - `USDT`
    
    - `WBTC`
    
    - `WETH`
    
      default value is all of the ftoken vaults registry
    

# examples

- list all registry of vaults

    ```sh
    list-registry-of-erc20s 
    ```

- list registry of vaults of `USDT`

    ```sh
    list-registry-of-vaults USDT
    ```