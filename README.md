# TiGr-Bot

An NFT focused Telegram bot that uses Account Abstraction to remove all trust from the Telegram bot.

🏗️ TODO what TiGr bot does

Tiger Bot is a telegram bot that simplifies buying and selling NFTs. The bot allows any user with a telegram account to buy and sell NFTs without ever having to leave the TG. 

### The Problem 

Crypto UX has been a major stumbling block for mass adoption. There are 2 applications whose UX has catapulted them into the top 20 dapps by fees on Ethereum- Maestro and Unibot. These 2 TG bots pioneered the telegram sniper bot, making sniping tokens/copy trading on DEX’s all achievable within tg itself. 

Seeing the popularity of these bots has resulted in an explosion of telegram bots. While the UX convenience has outweighed the security risks associated with using these TG bots, the security risks are a very real concern. 

All of the TG bots use burner wallets, which users are required to deposit funds into. The private keys for these wallets are held by the bot, making it a custodial wallet. As we have now been reminded multiple times, not just in crypto, but also with banks- custodial flows are only as good as the custodian. 

This is against the ethos of decentralization. Beyond the ethos, it isn't good for business. Trust minimization is the only anti-fragile measure in place that protects users from the inevitability of Murphy's law. 

While centralized custodians like coinbase are heavily regulated, it would be difficult to identify any form of legal recourse in the event something were to go wrong with the TG bots. 

So while these TG bots seem to look great at the moment, they are built on a house of cards, and on the fragility of Trust. 

This is the problem we aim to solve.

![8-zEO91d7rVxDcjL9](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/6d8588b8-424a-40a5-ae16-53919823069f)

## Problem solved by project

🏗️ TODO Problem

🏗️ TODO How TiGr bot solves the problem

For an indepth description of the logic flow see [https://github.com/superhack-eu091/SafeDelegatedProxy](https://github.com/superhack-eu091/SafeDelegatedProxy#logic-flow-for-telegram-bot--safe-smart-contract-wallet-interactions).

## Media

🏗️ TODO VIDEO

🏗️ TODO SCREENSHOTS

## Hackathon codebase

* Telegram bot https://github.com/superhack-eu091/tigr-bot-interface
* Safe delegated ERC721 Proxy and other smart contracts https://github.com/superhack-eu091/SafeDelegatedProxy

## Deployed Contracts

Full listing of all contracts in https://github.com/superhack-eu091/tigr-bot-interface/blob/main/src/config/project-configs.json

### Goerli
* safeDelegateProxy https://goerli.etherscan.io/address/0xD3F41eE51AAF27baada9A75F5ECfc282EF7529FF
* mockMarket https://goerli.etherscan.io/address/0xb4f19bC25D2c31A109eb620973B693bE2029147e

### Optimism Goerli
* safeDelegateProxy https://goerli-optimism.etherscan.io/address/0xf57E07F9883DdE92DE7fD7fdD66a21B58980f541
* mockMarket https://goerli-optimism.etherscan.io/address/0x71efD4dD2Aa261F259041122A4249735858AFFEb

### Base Goerli
* safeDelegateProxy https://goerli.basescan.org/address/0x01550034cAEC5e97B6980294319eb6d02cc8A25D
* mockMarket https://goerli.basescan.org/address/0x6e4317694661BBd113Fd3907Dd0E34A6acFcac17

### Zora Goerli
* safeDelegateProxy https://testnet.explorer.zora.energy/address/0x01550034cAEC5e97B6980294319eb6d02cc8A25D
* mockMarket https://testnet.explorer.zora.energy/address/0x583F14CE08a95D30E681a5848CC6835992D0386B

## Team

* Vishwa Naik
* Konrad Strachan https://github.com/konradstrachan
* David Perez Negron https://github.com/P1R
* Jason Garcia https://github.com/jasonjgarcia24
* Sarat Angajala https://github.com/SaratAngajalaoffl
