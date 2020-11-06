# list-registry-of-erc20s

list registry of supported erc20s

# usage

```sh
list-registry-of-erc20s <TOKEN_SYMBOL> 
```

- `<TOKEN_SYMBOL>`(optional): can be one of the following
  
    - `USDT`
    
    - `WBTC`
    
    - `WETH`
    
      default value is all of the erc20s contract registry
    

# examples

- list all registry of erc20s

    ```sh
    list-registry-of-erc20s 
    ```

- list registry of `USDT`

    ```sh
    list-registry-of-erc20s USDT 
    ```