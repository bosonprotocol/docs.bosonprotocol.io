---
layout: docs
title: "Boson Protocol: Docs: Protocol Overview: How Boson Works"
short_title: "How Boson Works"
permalink: /protocol-overview/how-boson-works/
---

# How Boson works

## Overview

Boson is a _permissionless market exchange protocol_, which handles dispute
mediations and reversals in order to facilitate P2P transactions for physical
items in a trustless way. By leveraging a dynamic game, the protocol enables
practically atomic automated transactions. It is implemented in a system of
non-upgradeable smart contracts on the [Ethereum](https://ethereum.org/)
blockchain. The protocol functions as a commercial primitive or building block,
thereby enabling digital and decentralized applications to be easily developed
on top of it. This obviates the requirement for trusted intermediaries; instead
prioritizing decentralization, cost minimization and trustless value exchange.

## Core exchange mechanism

Boson Protocol’s core mechanism is a type of sequential game in which buyer and
seller commit deposits up-front. The game rules and the final deposit transfer
scheme are designed to coordinate transactions and incentivize parties to behave
fairly. Or more formally, we say that: "subgame perfect equilibrium
implementation corresponds to the honest behavior of both players."

The following image illustrates the complete game tree:

![/images/docs/game-tree.png](/images/docs/game-tree.png)

## How It Works

When a seller lists an item, they specify the item price as well as deposit
amounts for both the buyer and seller. In addition to this, the desired payment
currency and the listing's validity period are detailed. This validity period
includes the start date and expiry date of the listing, the first of which is
the date from when this item can be redeemed. This mints a voucher set following
the ERC-1155 NFT standard. The seller pays their deposit as part of the listing
process, placing it in escrow.

When a buyer commits to purchase an item, they pay the seller-defined deposit
and the item price, placing both in escrow. This extracts a voucher from the
voucher set, following the ERC-721 NFT standard. The buyer then has the option
to redeem their purchased item (i.e. gaining ownership of said item). At this
point, the payment amount is released to the seller. Both the buyer and seller
deposits are released to the relevant party after the wait period expires.

Instead of redeeming, the buyer can choose to either refund their purchase or
let the voucher expire. Furthermore, after doing this (or redeeming) they can
choose to complain about the purchase. At any point, the seller has the option
to cancel the transaction; if they choose to do so after the buyer has redeemed,
this is deemed as accepting fault. The buyer still has the option to complain
after this, provided that they have not already done so earlier in the process.
Each of these options, in addition to the voucher expiring, results in a
variance in payouts for both the buyer and seller.

<img src="/images/docs/token-lifecycle-light.png"
     alt="Token lifecycle"
     class="block dark:hidden"/>
<img src="/images/docs/token-lifecycle-dark.png"
     alt="Token lifecycle"
     class="dark:block hidden"/>

## Note on beta

This is very much our beta launch of our mechanism and the first step in our
work for bringing greater trust and protection to buyers in dCommerce to allow
them to benefit from the promises of interoperability, specialized flows from
composable pieces, and of course protection from all the extractive ills of
intermediaries.
