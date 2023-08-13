# TiGr-Bot

Pronounced : tiger 🐅

A bot that uses Account Abstraction to provide a true Defi experience buying and selling NFTs via Telegram without any additional trust assumptions or loss of control over funds or NFTs.

This project was build for the ETH Global SuperHack virtual Hackathon.

![image](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/55d354fa-fb92-4519-b169-c98c63f70bd6)

## Overview

![tg without the trust](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/4b6022ac-5d0d-45ac-a00e-3242b2e84ce4)

### tl;dr

#### What's the problem with Telegram bots now?

Telegram bots require users to deposit funds into wallets the bots create for them. For example, this is the welcome message from the most popular Telegram bot UNIBOT. It generates wallets for each new user that it controls and requires funds to be moved in to them.

![image](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/0be047ff-dd1f-4ed1-9d3c-b5257d4cdb0b)

When users send funds to addresses controlled by bots they give up all ability to control these funds and leave Defi for a CEX like experience with closed source bots controlling their funds.

![image](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/abf5d1d7-0fe3-4f25-8b7e-a43cc9ae57c5)

Not your keys not your crypto - the Telegram experience of interacting with funds is great, the security trade offs are not

#### How does TiGr bot solve this?

TiGr is a bot that gives users the same UX as any other Telegram bot, but doesn't require the user to send any funds to addresses controlled by the bot. The TiGr bot will work with any Safe smart contract wallet a user already has on any chain and allows the user to keep control of their funds and explicitly define how the bot can use them.

No more will a bot have access to all funds and NFTs - with TiGr bot and the delegate smart contract Safe module, users can specify which NFTs they are happy to buy and sell and exactly the maximum price they are prepared to buy for, or the minimum they expect to get when they sell.

Awesome Telegram UX + security and flexibility of a SAFE smart contract wallet

### In detail

TiGr is an NFT focused Telegram bot that uses Account Abstraction to remove all trust from Telegram and provide a true Defi experience through self sovereign verifyable actions.

#### The Problem 

Crypto UX has been a major stumbling block for mass adoption. There are 2 applications whose UX has catapulted them into the top 20 dapps by fees on Ethereum- Maestro and Unibot. These 2 TG bots pioneered the telegram sniper bot, making sniping tokens/copy trading on DEX’s all achievable within tg itself. 

Seeing the popularity of these bots has resulted in an explosion of telegram bots. While the UX convenience has outweighed the security risks associated with using these TG bots, the security risks are a very real concern. 

All of the TG bots use burner wallets, which users are required to deposit funds into. The private keys for these wallets are held by the bot, making it a custodial wallet. As we have now been reminded multiple times, not just in crypto, but also with banks- custodial flows are only as good as the custodian. 

This is against the ethos of decentralization. Beyond the ethos, it isn't good for business. Trust minimization is the only anti-fragile measure in place that protects users from the inevitability of Murphy's law. 

While centralized custodians like coinbase are heavily regulated, it would be difficult to identify any form of legal recourse in the event something were to go wrong with the TG bots. 

So while these TG bots seem to look great at the moment, they are built on a house of cards, and on the fragility of Trust. 

This is the problem TiGr solves.

#### The Solution 

Using Account Abstraction via a SAFE smart contract wallet module extension we have created a system where a Telegram bot needs only to be granted allowances to perform actions on the user's behalf like swapping tokens or interacting with defi contracts. We have built an NFT trading bot that allows the user to trade NFTs. When the user connects their wallet to the bot (done simply by pasting their ENS or Safe wallet address) they can set conditions on anything the bot can do on their behalf.

For example, a user can give access to the Bot to buy a specific NFT from a certain marketplace, but restrict the maximum amount the Bot can take in exchange. When this is triggered by the bot the swap of funds for the NFT is performed atomically further eliminating any trust the user needs to place in the Telegram bot. The same holds true for selling NFTs.

The way this works is we have created a Safe Delegate module that connects to a user's SAFE smart contract wallet. Interactions between tokens and NFTs are driven by this flow with the user using a front end to select what they want to buy and sell and for how much which will set the allowances. Once these allowances are set, they can use the Telegram bot to execute the buying or selling of NFTs directly without any further wallet interaction and no additional trust assumptions or access to funds.

![Flows](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/259900a7-083f-4aab-ace7-1a4931202cd5)

For an indepth description of the logic flow see [https://github.com/superhack-eu091/SafeDelegatedProxy](https://github.com/superhack-eu091/SafeDelegatedProxy#logic-flow-for-telegram-bot--safe-smart-contract-wallet-interactions).

## Media
![TelegramBotTiGr](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/83315a04-a7fc-49e2-ba3c-3e8cde852075)

See https://ethglobal.com/showcase/in-tgr-j0imz for more screenshots and videos.

### Demo of contract interactions

![image](https://github.com/superhack-eu091/TiGr-Bot/assets/21056525/a5e75e8a-5cf1-4821-8a61-7a9bb8a79e4c)

Found in [smart contract repo](https://github.com/superhack-eu091/SafeDelegatedProxy/raw/main/TiGr%20Bot%20narrated.mp4)

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
