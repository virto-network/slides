---
title: "Unlocking Parachain Potential: Integrating ink! Smart Contracts with Chain Extensions"
description: This workshop is designed to equip you with the skills to prepare your parachain for ink!-based smart contracts using Chain Extensions. You’ll learn how to configure your chain, create and deploy smart contracts, and test their functionality, all through hands-on exercises.
duration: 30 minutes
---

# Unlocking Parachain Potential: Integrating ink! Smart Contracts with Chain Extensions

---

## What do you need?

<pba-flex center>

- `cargo-contract`
- `zombienet`
- Want to have fun!

</pba-flex>

---v

### `cargo-contract`

<https://use.ink/getting-started/setup/>

---v

### `zombienet`

<https://paritytech.github.io/zombienet/install.html#using-npm>

---

## Chain Extensions

![Venn Diagram between ink! and Parachain Runtime](https://use.ink/img/venn.png)<!-- .element: style="width: 50%" -->

---v

### It's all about passing messages

```mermaid
sequenceDiagram
    actor User
    participant Contract as Smart Contract
    participant ChainExtensions as Chain Extensions
    participant Pallet

    User ->> Contract: contract_method
    
    Contract ->> ChainExtensions: do_get_attribute "attendance_type"
    activate ChainExtensions
      ChainExtensions ->> Pallet: pallet_method
        
      activate Pallet
        Pallet ->> ChainExtensions: response
      deactivate Pallet

      ChainExtensions ->> Contract: response
    deactivate ChainExtensions

    Contract ->> User: Yaay!
```

---

## What can YOU do with Chain Extensions?

Depends… who are you?

---v

### As a Runtime Developer

Design an API that allows contract developers to extend what your users can do on your blockchain.

---v

### As a Contract Developer

Interact with the blockchain via a more specialized _"API"_.

---v

### Today we are both

---v

![Uncle Ben](https://media.tenor.com/Hz0fHyUQzfwAAAAe/spider-man-uncle-ben.png)

---

## What we're doing today?

---v

```mermaid
sequenceDiagram
    participant Contract as Smart Contract
    participant ChainExtensions as Chain Extensions
    participant Pallet as Nfts

    Contract ->> Contract: constructor
    Contract ->> ChainExtensions: create_nft_collection
    activate ChainExtensions
      ChainExtensions ->> Pallet: create
        
      activate Pallet
        Pallet ->> ChainExtensions: collection_id
      deactivate Pallet

      ChainExtensions ->> Contract: collection_id
    deactivate ChainExtensions

    Contract ->> Contract: store collection_id
```

---v

```mermaid
sequenceDiagram
    actor User
    participant Contract as Smart Contract
    participant ChainExtensions as Chain Extensions
    participant Pallet as Nfts
    
    User ->> Contract: airdrop_nft
    
    Contract ->> ChainExtensions: create_item
    activate ChainExtensions
      ChainExtensions ->> Pallet: mint
        
      activate Pallet
        Pallet ->> ChainExtensions: item_id
      deactivate Pallet

      ChainExtensions ->> Contract: item_id
    deactivate ChainExtensions

    Contract ->> User: "Your NFT has been created with ID ${item_id}"
```

---v

### Let's get to the code

<https://github.com/pandres95/ink-chain-extensions-demo>
