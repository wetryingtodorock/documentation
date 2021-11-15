---
layout: nodes.liquid
section: smartContract
date: Last Modified
title: "Contract Addresses"
permalink: "docs/vrf-deployments/"
metadata:
  title: "Chainlink VRF Contract Addresses"
  image:
    0: "/files/OpenGraph_V3.png"
---

> ℹ️ You are viewing the VRF v2 guide.
>
> If you are using v1, see the [VRF v1 guide](./v1).

Chainlink VRF allows you to integrate provably-fair and verifiably random data in your smart contract.

For implementation details, read [Introduction to Chainlink VRF](../chainlink-vrf/).

# Coordinator Parameters
These parameters are configured by the coordinator owner, which currently is Chainlink itself until the threshold VRF is released. 

You can view their values by running `getConfig` on the coordinator.
- `uint16 minimumRequestBlockConfirmations` - A minimum number of confirmation blocks on VRF requests before oracles should respond.
- `uint32 maxGasLimit` - The maximum gas limit supported for a fulfillRandomWords callback.
- `uint32 stalenessSeconds` - How long we wait until we consider the ETH/LINK price (used for converting gas costs to LINK) is stale and use `fallbackWeiPerUnitLink`
- `uint32 gasAfterPaymentCalculation` - How much gas is used outside of the payment calculation. Specifically its the gas outside of here (TODO link) and here (TODO link).

# Fee parameters
Also configured by the coordinator owner, these specify the billing tranches based on request count. 
You can view them by running `getFeeConfig` on the coordinator. 
- `uint32 fulfillmentFlatFeeLinkPPMTier1`, `uint32 fulfillmentFlatFeeLinkPPMTier2`, `uint32 fulfillmentFlatFeeLinkPPMTier3`, `uint32 fulfillmentFlatFeeLinkPPMTier4`, `uint32 fulfillmentFlatFeeLinkPPMTier5` - fees for each tier specified in millionths of LINK.
- `uint24 reqsForTier2`, `uint24 reqsForTier3`, `uint24 reqsForTier4`, `uint24 reqsForTier5` - tier boundaries in terms of requests made using a given subscription.

# Polygon (Matic) Mainnet

|Item|Value|
|---|---|
|LINK Token|`TODO`|
|VRF Coordinator|`TODO`|
|Key Hash|`TODO`|

# Polygon (Matic) Mumbai Testnet

|Item|Value|
|---|---|
|LINK Token|`0x326C977E6efc84E512bB9C30f76E30c160eD06FB`|
|VRF Coordinator|`0xb96A95d11cE0B8E3AEdf332c9Df17fC31D379651`|
|100 gwei Key Hash|`0x4b09e658ed251bcafeebbc69400383d49f344ace09b9576fe248bb02c003fe9f`|
|500 gwei Key Hash|`0x85ebe225389765a0f6256c01b0ffab64c2e3eee50527cca47800417218b84b47`|

# Binance Smart Chain Mainnet

|Item|Value|
|---|---|
|LINK Token|`TODO`|
|VRF Coordinator|`TODO`|
|Key Hash|`TODO`|

# Binance Smart Chain Testnet

|Item|Value|
|---|---|
|LINK|`0x84b9B910527Ad5C03A9Ca831909E21e236EA7b06`|
|VRF Coordinator|`0xb96A95d11cE0B8E3AEdf332c9Df17fC31D379651`|
|20 gwei Key Hash|`0xbed0624a3355d6c02f88cfa96054e0d39b788c380fdf7e14063edea8ba624d7dT`|
|50 gwei Key Hash|`0xd4bb89654db74673a187bd804519e65e3f71a52bc55f11da7601a13dcf505314`|


# Ethereum Mainnet

|Item|Value|
|---|---|
|LINK Token|`TODO`|
|VRF Coordinator|`TODO`|
|Key Hash|`TODO`|

# Rinkeby

> 🚰Rinkeby Faucets
>
> Testnet LINK is available from https://faucets.chain.link/rinkeby
> Testnet ETH is available from: https://faucets.chain.link/rinkeby
> Backup Testnet ETH Faucets: https://faucet.rinkeby.io/, https://rinkeby-faucet.com/, https://app.mycrypto.com/faucet

|Item|Value|
|---|---|
|LINK|`0x01BE23585060835E02B77ef475b0Cc51aA1e0709`|
|VRF Coordinator|`0x5Ff6db248780a059ad893c898ba9a198Eddc4a08`|
|10 gwei Key Hash|`0x59245bc7b65da15a2d4328d176535e11d9675cd7cf13fcb800eb7277da216a36T`|
|30 gwei Key Hash|`0xd89b2bf150e3b9e13446986e571fb9cab24b13cea0a43ea20a6049a85cc807cc`|