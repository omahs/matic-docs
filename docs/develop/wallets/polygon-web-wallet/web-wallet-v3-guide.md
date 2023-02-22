---
id: web-wallet-v3-guide
title: Polygon Wallet Suite
sidebar_label: Usage Guide
description: Learn how to use the Polygon Wallet Suite
keywords:
  - wallet
  - matic
  - docs
  - wiki
  - polygon
  - guide
  - web wallet
  - v3
image: https://wiki.polygon.technology/img/polygon-wiki.png
---

import useBaseUrl from '@docusaurus/useBaseUrl';

**A new version of our Polygon Wallet is live**. Now called **Polygon Wallet Suite**, our new environment provides a more seamless experience with great improvements on the user interface as well as on its overall experience.

This guide shows instructions to deposit and withdraw funds using [Polygon Wallet Suite](https://wallet.polygon.technology/). For performing those actions, you need to connect a wallet to Polygon's environment. In this tutorial, we used Metamask, but Polygon is integrated with other wallets such as Coinbase, Bitski, Venly and WalletConnect.

:::tip

Please refer to [<ins>this guide</ins>](/develop/metamask/config-polygon-on-metamask.md) to learn how to connect Polygon to Metamask.
:::

## Logging into the Polygon Wallet Suite

To log into the Polygon Wallet Suite you need to access the following URL: https://wallet.polygon.technology/.

Once you connect your account with the Web Wallet, you will be taken to the landing page with various means on how to transact with the web wallet. Polygon PoS chain currently offers the following services:

- **Polygon Wallet**: for sending, receiving and storing your assets on the Polygon network
- **Polygon Bridge**: for withdrawals and deposits across networks
- **Polygon Staking**: your go-to place for staking and getting rewards with your MATIC tokens
- and the **Polygon Safe Bridge**.

Click on the Polygon Wallet or Polygon Bridge, and you will see all your token balances on the Polygon Wallet across the bridges (PoS and Plasma).

<img src={useBaseUrl("img/wallet/v3/landing-page.png")} width="100%" height="100%"/>

:::tip Metamask

Be attentive to all Metamask's popups. Throughout the deposit and withdrawal processes, you will be prompted with Metamask's popups to confirm transactions, switch networks and other procedures. You can only proceed with those transactions if you confirm the actions on Metamask.

::: 

## Deposit Funds from Ethereum to Polygon

You can either watch the **video tutorial** here or follow the **step-by-step guide** provided below.

<div align="center">
  <video loop autoplay width="70%" height="70%" controls="true" >
    <source type="video/mp4" src="/img/wallet/v3/deposit/deposit-polygon-wallet.mp4"></source>
    <p>Your browser does not support the video element.</p>
  </video>
</div>

#### Step-by-Step Guide

1. Click on the **Move Funds from Ethereum to Polygon** button or on the **Deposit** button from any of the token types in the **Token** Balance** section.

  <img src={useBaseUrl("img/wallet/v3/deposit/balances.png")} width="1000" height="1000" />

2. You will be redirected to the bridge page where you need to enter the deposit amount.

  <img src={useBaseUrl("img/wallet/v3/deposit/bridge.png")} width="100%" height="100%"/>

  :::note

  The **transfer mode** will be enabled based on the token chosen.

  :::

3. Once you have added the amount that you want to deposit, you can then click on the **Transfer** button. After you click on the **Transfer** button, you need to click on the **Continue** button on the next popup.
  
  <div align="center"><img src={useBaseUrl("img/wallet/v3/deposit/please-note.png")} width="50%" height="50%"/></div>

  You will see a **Transfer Overview** popup with an estimate of the total gas required for the transaction:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/deposit/transfer-overview.png")} width="50%" height="50%" /></div>

  After that, you can review your transaction details:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/deposit/review-transfer.png")} width="50%" height="50%" /></div>

4. Once you confirm the transaction, you will see a **Transfer in Progress** popup which will show you the Deposit status. It will take ~7-8 minutes for the tokens to show up on Polygon.

5. After the required time, the transaction will be completed.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/deposit/completed.png")} width="50%" height="50%" /></div>

You can always check your past and current transactions by clicking on the **Transactions** tab on the left.

##  Withdraw Funds from Polygon to Ethereum

### On Polygon PoS Bridge

Withdrawing funds from Polygon back to the Ethereum Mainnet via PoS Bridge is an extremely simple process. For the funds to be available back on Ethereum it will take from 45 minutes to 3 hours. You can either watch the **video tutorial** here or follow the **step-by-step guide** provided below.

<div align="center">
  <video loop autoplay width="70%" height="70%" controls="true" >
    <source type="video/mp4" src="/img/wallet/v3/pos/withdraw-polygon-wallet.mp4"></source>
    <p>Your browser does not support the video element.</p>
  </video>
</div>

#### Step-by-Step Guide

1. To withdraw funds, click on the **Withdraw** option on any of the tokens from the **Token Balance** section.

  <img src={useBaseUrl("img/wallet/v3/pos/balances.png")} width="100%" height="100%"/>

2. You will be redirected to the Bridge page where you need to enter the Withdrawal amount.

  <img src={useBaseUrl("img/wallet/v3/pos/bridge.png")} width="100%" height="100%" />

  :::note

  The **transfer mode** will be enabled based on the token chosen.

  :::

3. Once you have added the amount that you want to withdraw, you can then click on the **Transfer** button. After you click on the **Transfer** button, you need to click on the **Continue** button on the next popup.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/please-note.png")} width="50%" height="50%" /></div>

  You will see a **Transfer Overview** popup with an estimate of the total gas required for the transaction:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/transfer-overview.png")} width="50%" height="50%"/></div>

  After that, you can review your transaction details:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/review-transfer.png")}  width="50%" height="50%"/></div>

4. Once the transaction is approved, you will see a popup on your screen like this:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/transaction-progress.png")} width="50%" height="50%"/></div>

  The first transaction is to initiate your withdrawal. You need to wait for the checkpoint to arrive. This could take up to 3 hours to complete.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/waiting-checkpoint.png")} width="50%" height="50%"/></div>

5. Once the checkpoint has arrived, you will need to **confirm the second transaction**. Then, when you have confirmed the second transaction, you will receive your funds back on Ethereum.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/pos/completed.png")} width="50%" height="50%"/></div>

### On Plasma Bridge

Withdrawing funds from Polygon back to the Ethereum mainnet via Plasma Bridge is a simple process but with a **challenge period**. You can either watch the **video tutorial** here or follow the **step-by-step guide** provided below.

<div align="center">
<video loop autoplay width="70%" height="70%" controls="true" >
  <source type="video/mp4" src="/img/wallet/v3/plasma/withdraw-plasma-v3.mov"></source>
  <p>Your browser does not support the video element.</p>
</video>
</div>

#### Step-by-step guide

1. To withdraw funds, click on the **Withdraw** link from any of the Plasma token types on **Your tokens** on the **Polygon Mainnet** section.

  <img src={useBaseUrl("img/wallet/v3/plasma/balances.png")} width="100%" height="100%"/>

2. You will be redirected to the Bridge page where you need to enter the **Withdraw Amount**.

  <img src={useBaseUrl("img/wallet/v3/plasma/bridge.png")} width="100%" height="100%"/>

3. Once you have added the amount that you want to withdraw, you can then click on the **Transfer** button. After that, you need to click on the **Continue** button on the next popup.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/please-note.png")} width="50%" height="50%" /></div>

  You will see a **Transfer Overview** popup with an estimate of the total gas required for the transaction:

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/transfer-overview.png")} width="50%" height="50%"/></div>

  Click on the **Continue** button from the **Transfer Overview** popup and you will see a popup opening, similar to the previous one where you can review your transaction details.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/review-transfer.png")} width="50%" height="50%" /></div>

  This will be the first of 3 transactions that will need to be completed.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/transfer-progress.png")} width="50%" height="50%"/></div>

4. The first transaction is to initiate your withdrawal. Once the withdrawal transaction is initiated, you need to wait for the checkpoint to arrive. This could take up to 3 hours to complete.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/checkpoint-arrived.png")} width="50%" height="50%"/></div>

5. Once the checkpoint has arrived, you need to confirm a new transaction to enter the **7-day challenge period**.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/challenge-completed.png")} width="50%" height="50%"/></div>

6. To get funds back to Ethereum you will need to confirm one last time. Once you have confirmed all these transactions, you will receive your funds back on Ethereum.

  <div align="center"><img src={useBaseUrl("img/wallet/v3/plasma/transfer-completed.png")} width="50%" height="50%"/></div>

## Swap for Gas

The MATIC token is used for paying gas fees in the Polygon ecosystem. It's always important to have a minimum amount of MATIC to perform transactions on Polygon. **In fact, 0.01 MATIC can pay for about 20 transactions**. There are a few ways you can acquire MATIC tokens:

- buy them using Fiat On-ramp platforms,
- swap for other tokens, or
- trade them on a supported exchange.

Polygon also offers the possibility of swapping tokens for MATIC. You can currently choose from a range of cryptocurrencies to swap for MATIC, namely ETH, USDC, USDT, and others.

:::tip

This is a gasless transaction. You do not have to pay any gas fees.

:::

You can either watch the video tutorial below or follow the step-by-step guide.

<div align="center">
<video loop autoplay width="70%" height="70%" controls="true" >
  <source type="video/mp4" src="/img/wallet/v3/swap-gas.mp4"></source>
  <p>Your browser does not support the video element.</p>
</video>
</div>

#### Step-by-step guide

1. Assuming you are on the assets homepage, find the **Swap for Gas** feature on the sidebar on your left.

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-gas-home.png")} /></div>

2. Now, you need to set the amount of MATIC you need, either by choosing one of the given quantities or entering the amount you need (1). You should also select the token that will be swapped for MATIC (2). **The minimum amount for requesting MATIC tokens is 0.5 MATIC**.
  <div align="center"><img src={useBaseUrl("/img/wallet/swap-gas-tokens.png")} width="400"/></div>

3. MetaMask will then prompt you to sign the transaction. If you haven't added the Polygon network to your Metamask, you will be prompted to install it. Please proceed with the installation or check out this guide [here](/develop/metamask/config-polygon-on-metamask.md).

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-gas-signature.png")} width="400"/></div>

  :::note

  If the **Sign** button is not visible, try scrolling down by clicking on the down arrow in the **Message** field.

  :::

4. After you signed it, you will be able to transfer the requested amount of MATIC to your wallet.

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-gas-transfer.png")} width="400"/></div>

5. A new signature will be requested:

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-gas-sign-swap.png")} width="400"/></div>

  Transaction completed. Remember that you can always verify it on [Polygonscan](https://polygonscan.com/)!


## Token Swap

You can swap tokens for other tokens using the **Token Swap** feature, which uses decentralized exchanges under the hood. The Token Swap feature may be found in the Wallet Suite side menu.

<div align="center"><img src={useBaseUrl("/img/wallet/swap-token-home.png")}/></div>
<br/>

You can either watch the video tutorial here or follow the step-by-step guide provided below.

<div align="center">
<video loop autoplay width="70%" height="70%" controls="true" >
  <source type="video/mp4" src="/img/wallet/v3/swap-token.mp4"></source>
  <p>Your browser does not support the video element.</p>
</video>
</div>

#### Step-by-step guide

1. The token on the top is the one you are swapping. The other one on the bottom is what you are going to receive.

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-token.png")} width="400"/></div>

2. Review the transaction before it goes through.

  <div align="center"><img src={useBaseUrl("/img/wallet/swap-token-review.png")} width="400"/></div>

3. **Sign** and confirm the transaction on MetaMask and the transaction will be completed successfully.

## Token Lists

You can customize the list of tokens you may see on the Polygon Wallet Suite homepage. For that, click on **Manage Token List**:

<div align="center"><img src={useBaseUrl("/img/wallet/token-list-home.png")} /></div>
<br/>

There are some default options provided by Polygon, but you can always add new token lists by entering their URLs.

:::tip

You can find some of the token lists here: https://tokenlists.org/

:::

<div align="center"><img src={useBaseUrl("/img/wallet/token-list-manage.png")} width="400" />
</div>
<br/>

You can also **make your own list**, import it to Polygon Wallet and even share it with the community.
To learn more about creating your own token lists, check out this guide to [Authoring Token Lists on Github](https://github.com/uniswap/token-lists#authoring-token-lists). 

:::note

The **Chain ID should be 137** when creating a Polygon list.

:::

If you need to add a token to one of our lists, [<ins>add a Token Request</ins>](https://github.com/maticnetwork/polygon-token-list/issues/new?assignees=&labels=add+token+request&template=add_token_request.md&title=Add+%7BTOKEN_SYMBOL%7D%3A+%7BTOKEN_NAME%7D) with the required information, and it’ll be reviewed by our team.

:::caution

As it is fairly easy to [<ins>add custom tokens</ins>](faq/adding-a-custom-token.md), users should always do their research and only choose trustworthy projects/tokens.

:::
