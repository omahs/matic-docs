---
id: torus
title: Torus
description: Torus is a non-custodial key management system for dApps
keywords:
  - wiki
  - polygon
  - torus
  - wallet
  - guide
  - dApp
image: https://wiki.polygon.technology/img/polygon-wiki.png
---

Torus is a user-friendly, secure, and non-custodial key management system for decentralized apps. We're focused on providing mainstream users a gateway to the decentralized ecosystem.

**Type**: Non-custodial / HD <br/>
**Private Key Storage**: User’s local browser storage / Encrypted and stored on Torus servers <br/>
**Communication to Ethereum Ledger**: Infura <br/>
**Private key encoding**: Mnemonic / Social-Auth-login <br/>

Depending on your application needs, Torus can be integrated via the Torus Wallet, or by interacting directly with the Torus Network via CustomAuth. For more information, visit the [Torus documentation](https://docs.tor.us/).

## Torus Wallet Integration

If your application is already compatible with MetaMask or any other Web3 providers, integrating the Torus Wallet would give you a provider to wrap the same Web3 interface. You can install via a npm package. For more ways and in-depth information, please visit the official Torus documentation on [wallet integration](https://docs.tor.us/wallet/get-started).

### Installation

```bash
npm i --save @toruslabs/torus-embed
```

### Example

```js title="torus-example.js"
import Torus from "@toruslabs/torus-embed";
import Web3 from "web3";

const torus = new Torus({
  buttonPosition: "top-left" // default: bottom-left
});

await torus.init({
  buildEnv: "production", // default: production
  enableLogging: true, // default: false
  network: {
    host: "mumbai", // default: mainnet
    chainId: 80001, // default: 1
    networkName: "Mumbai Test Network" // default: Main Ethereum Network
  },
  showTorusButton: false // default: true
});

await torus.login(); // await torus.ethereum.enable()
const web3 = new Web3(torus.provider);
```

## CustomAuth Integration

If you are looking to control your own UX, from login to every interaction, then you can use CustomAuth. You can integrate via one of their SDKs depending on the platform(s) you are building on. For more info, please visit [Torus CustomAuth integration](https://docs.tor.us/customauth/get-started).
