---
id: l2-transaction-cycle-intro
title: Submitting Transactions in zkEVM
sidebar_label: Submit Transaction
description: A guide to help developers understand the transaction life cycle in zkEVM.
keywords:
  - docs
  - zk rollups
  - polygon
  - zkEVM
  - zkevm protocol
  - deploy on zkEVM
  - Polygon zkEVM
image: https://wiki.polygon.technology/img/thumbnail/polygon-zkevm.png
---

:::info

This document series describes in detail the various forms and stages that L2 users' transactions go through, from the time they are created in users' wallets to the time they are finally verified with indisputable evidence on L1.

:::

Transactions in the Polygon zkEVM network are created in users' wallets and signed with their private keys.

Once generated and signed, **the transactions are sent to the Trusted Sequencer's node via their JSON-RPC interface**. The transactions are then stored in the **pending transactions pool**, where they await the Sequencer's selection for execution or discard.

**Users and the zkEVM communicate using JSON-RPC, which is fully compatible with Ethereum RPC**. This approach allows any EVM-compatible application, such as wallet software, to function and feel like actual Ethereum network users.
