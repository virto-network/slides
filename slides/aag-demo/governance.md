---
title: Governance at Kreivo Communities
description: This slides let audience understand how to use governance in Kreivo parachain
duration: 2.5 minutes
---

# Governance at Communities

---

## What is a community?

Is a self-governed entity with a sovereign account that can act on-chain via governance actions

---

<pba-cols>

<pba-col>

## Before Kreivo

<pba-flex center>

- Multisig<!-- .element: class="fragment" data-fragment-index="0" -->
- Off-chain<!-- .element: class="fragment" data-fragment-index="1" -->

</pba-flex>

</pba-col>

<pba-col>

## After Kreivo

<pba-flex>

<ul>
  <li>
  
  `referenda::submit`
  
  </li><!-- .element: class="fragment" data-fragment-index="3" -->
  <li>
  
  `communities::vote`
  
  </li><!-- .element: class="fragment" data-fragment-index="4" -->
</ul>

</pba-flex>

</pba-col>

</pba-cols>

---

## Types of Governance in Kreivo

<pba-flex center>

- **Membership**
- **Native token**
- **Community Asset**
- **Ranked**

</pba-flex>

---v

### Membership

One memberhsip, one vote.

---v

### Native token

It's like [OpenGov](https://polkadot.network/features/opengov/).

---v

### Community Asset

Vote using your community-owned assets (`VIRTO`, `CUBO`, etc.)

---v

### Ranked

One membership, `n` votes, being `n` the voter's rank.

---

## Ok, but what's all of this for?

---v

### Community Management

Virtually every method you need to run to manage your community:

<pba-flex center>

- `communities::set_metadata`
- `communities::set_decision_method`
- `communities::add_member`
- `communities::remove_member`
- `communities::execute_as_community_account`

</pba-flex>

---v

### Use your community wallet

On Kreivo, every community has an `AccountId`. You can:

<pba-flex center>

- Own and admin community assets,
- Receive payments and make transfers on every asset available on **Asset Hub** (and **KSM**),
- Vote on Kreivo's Direction,
- … and many more!

</pba-flex>

---v

### Setup Smart Contracts

You'd be able to setup _Smart Contracts_ with `ink!` that run in an environment with access to handling **assets**, **nfts**, **payments**, and other communities' (and people's) accounts.

---v

### XCM

In the near-future, we'd support XCM Locations for every community on Kreivo. You'd have an account on Relay Chain, teleport assets, and execute operations on every major parachain on Kusama

All that through the enabled governance at your community.

---

# Questions?