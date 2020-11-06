# unstake-lptoken

Withdraw LP Tokens from the account. Please note that user will no longer able to receive FLAG rewards after withdrawing the LP tokens. 

# Usage

```sh
unstake-lptoken <TOKEN_SYMBOL> [AMOUNT]
```

- `<TOKEN_SYMBOL>`: can be one of the following

  - `USDT`
  - `WETH`
  - `WBTC`

  `AMOUNT` (optional): the amount of LP Tokens to withdraw, the default value is the current balance of LP tokens

# Example

Withdraw 0.01`WBTC` LP token from corresponding pool

```sh
unstake-lptoken WBTC 0.01 
```

## 
