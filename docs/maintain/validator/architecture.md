---
id: architecture
title: Architecture
description: Ethereum, Heimdall and Bor layers
keywords:
  - docs
  - matic
  - polygon
  - architecture
  - validator
slug: architecture
image: https://wiki.polygon.technology/img/polygon-wiki.png
---
import useBaseUrl from '@docusaurus/useBaseUrl';

The Polygon Network is broadly divided into three layers:

* **Ethereum layer** — a set of contracts on the Ethereum mainnet.
* **Heimdall layer** — a set of proof-of-stake Heimdall nodes running in parallel to the Ethereum mainnet, monitoring the set of staking contracts deployed on the Ethereum mainnet, and committing the Polygon Network checkpoints to the Ethereum mainnet. Heimdall is based on Tendermint.
* **Bor layer** — a set of block-producing Bor nodes shuffled by Heimdall nodes. Bor is based on Go Ethereum.

<img src={useBaseUrl("img/staking/architecture.png")} />

## Staking and Plasma smart contracts on Ethereum

To enable the [Proof of Stake (PoS)](/docs/home/polygon-basics/what-is-proof-of-stake) mechanism on Polygon, the system employs a set of [staking](/docs/maintain/glossary.md#staking) management contracts on the Ethereum mainnet.

The staking contracts implement the following features:

* The ability for anyone to stake MATIC tokens on the staking contracts on the Ethereum mainnet and join the system as a [validator](/docs/maintain/glossary.md#validator).
* Earn staking rewards for validating state transitions on the Polygon Network.
* Save [checkpoints](/docs/maintain/glossary.md#checkpoint-transaction) on the Ethereum mainnet.

The PoS mechanism also acts as a mitigation to the data unavailability problem for the Polygon sidechains.

## Heimdall (validation layer)

Heimdall layer handles the aggregation of blocks produced by [Bor](/docs/maintain/glossary.md#bor) into a Merkle tree and publishing the Merkle root periodically to the root chain. The periodic publishing of snapshots of the Bor sidechain are called [checkpoints](/docs/maintain/glossary.md#checkpoint-transaction).

For every few blocks on Bor, a validator on the Heimdall layer:

1. Validates all the blocks since the last checkpoint.
2. Creates a Merkle tree of the block hashes.
3. Publishes the Merkle root hash to the Ethereum mainnet.

Checkpoints are important for two reasons:

1. Providing finality on the root chain.
2. Providing proof of burn in withdrawal of assets.

An overview of the process:

* A subset of active validators from the pool is selected to act as [block producers](/docs/maintain/glossary.md#block-producer) for a [span](/docs/maintain/glossary.md#span). These block producers are responsible for creating blocks and broadcasting the created blocks on the network.
* A checkpoint includes the Merkle root hash of all blocks created during any given interval. All nodes validate the Merkle root hash and attach their signature to it.
* A selected [proposer](/docs/maintain/glossary.md#proposer) from the validator set is responsible for collecting all signatures for a particular checkpoint and committing the checkpoint on the Ethereum mainnet.
* The responsibility of creating blocks and proposing checkpoints is variably dependent on a validator’s stake ratio in the overall pool.

See also [Heimdall architecture](/docs/pos/heimdall/overview).

## Bor (block producer layer)

Bor is Polygon's sidechain block producer — the entity responsible for aggregating transactions into blocks.

Bor block producers are a subset of the validators and are shuffled periodically by the [Heimdall](/docs/maintain/glossary.md#heimdall) validators.

See also [Bor architecture](/docs/pos/bor/overview).
