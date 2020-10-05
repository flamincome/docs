# FlamIncome Terminal

[FlamIncome Terminal](https://flamincome.finance) provide a terminal UI for professional users.

Use [FlamIncome Web App](https://app.flamincome.finance/) or [Income Page of Flamingo](https://flamingo.finance/income) if you feel the terminal UI is uncomfortable.

# Guide

Users can type commands in FlamIncome Terminal UI for operations.

For more info about all the commands, see [FlamIncome Terminal Reference](https://docs.flamincome.finance/reference/terminal)

## Deposit Token to Flamincome

1. connect wallet

    ```sh
    connect-wallet
    ```

1. for example, deposit `1000` `USDT`, (if you want to deposit other tokens, replace `USDT` to another symbol) (if you want to deposit another amount, replace `1000` to your amount) (if you type `deposit-token-to-vault USDT` without the amount `1000`, the default amount will be your current balance)

    ```sh
    deposit-token-to-vault USDT 1000
    ```

1. (optional): type the following command to see the address of flamincomed token and add it to metamask (click the `Add Token` button on the `Assets`, then click `Custom Token` and paste the address into `Token Contract Address`)

    ```sh
    list-registry-of-vault
    ```

1. (optional): type the following command to see your flamincomed token balance

    ```sh
    get-balance-of-ftoken-by-symbol USDT
    ```

## Withdraw Token from FlamIncome

1. connect wallet

    ```sh
    connect-wallet
    ```

1. for example, withdraw `1000` `fUSDT`, (if you want to withdraw other tokens, replace `USDT` to another symbol) (if you want to withdraw another amount, replace `1000` to your amount) (if you type `withdraw-token-from-vault USDT` without the amount `1000`, the default amount will be your current balance of `fUSDT`)

    ```sh
    withdraw-token-from-vault USDT 1000
    ```