# get-earning-of-staking

* Query the amount of FLAG rewards obtained by the user

* This command is only used to display the amount of rewards obtained by the user. Use `claim-reward-of-staking` for actually claiming the reward. 

# Usage

```sh
get-earning-of-staking <TOKEN_SYMBOL> 
```

- `<TOKEN_SYMBOL>`: can be any of the following
  - `USDT`
  - `WETH`
  - `WBTC`

# Example

Check how many FLAG tokens you earn from staking WBTC LP tokens

```sh
get-earning-of-staking WBTC
```
