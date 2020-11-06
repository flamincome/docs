#  deposit-ftoken-to-normalizer 

* Convert ftokens to ntokens

* Must connect to wallet first

# Usage

``` 
deposit-ftoken-to-normalizer <TOKEN_SYMBOL> [DEPOSIT] [MINT]
```

Note: `TOKEN_SYMBOL` has no default value, thus you must enter an argument

`<TOKEN_SYMBOL>`: can be any of the following

- `USDT`
- `WETH`
- `WBTC`

`DEPOSIT`: the amount of fTokens you want to deposit

`MINT`: the amount of nTokens you want to get 

** It is recommended that you enter the same amount for deposit and mint.

## Example

1. Deposit 100 `fUSDT` and get 100 `nUSDT` 

   ```
   deposit-ftoken-to-normalizer USDT 100 100
   ```

