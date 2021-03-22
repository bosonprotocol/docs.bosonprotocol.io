---
layout: docs
title: "Boson Protocol: Docs: Protocol Overview: Ecosystem Participants"
short_title: "Ecosystem Participants"
permalink: /protocol-overview/ecosystem-participants/
---

# Ecosystem participants

## Seller

Elementary actor, representing the supply side. Seller makes an offer by minting
an ERC-1155 Voucher Set that holds a supply of a specified quantity of assets.

**Goals**: Offers goods and services and commits to their quality.

**Examples**: This could be an artist offering a physical counterpart to a
cryptoart NFT, or a clothing brand offering a physical counterpart to a wearable
in-game NFT.

## Buyer

Elementary actor, representing the demand side. A Buyer taking the offer is
implying that a singleton Voucher will be extracted from the originating Voucher
Set, thus minting an ERC-721.

**Goals**: Buys voucher to redeem later for goods or services.

**Examples**: This could be an art collector wanting to own and display the
physical artwork on their wall at home, or a gamer who is not only into
[crossplay](https://en.wikipedia.org/wiki/Cross-platform_play) but also
[cosplay](https://en.wikipedia.org/wiki/Cosplay).

## Aggregator

Custodial hub for multiple sellers. Aggregators enable sellers, as well as
perform basic curation based on their relationship with sellers.

**Goals**: Sources supply into BOSON network, get rewarded, can take an
additional transaction fee from the d2p transaction if appropriate (e.g. special
onboarding service, taking on deposits etc).

**Examples**: This could be a platform or a marketplace, but also independent
brokers who implement an appropriate front/backend logic for the Sellers they
are onboarding.

## Reseller

“Power buyer”. Has their own end-user app to roam the network and buy vouchers
in bulk to then resell later to their non-crypto customers.

**Goals**: Leverages Boson Protocol’s Voucher infrastructure for their B2C
logic.

**Examples**: This could be an art purveyor which focuses on NFT-keyed artwork
from particular artists, which looks for specific NFTs and then bundles them for
resale to galleries or at auctions directly.

## Developers / Projects

We have developed a reference frontend and backend for the v0.1 release. Our aim
is to enable and incentivize co-creation in the Boson Ecosystem. We are actively
engaged in token engineering and Web3 developer communities and will be offering
learning and co-creation opportunities to further the tokenomics, progressive
decentralization, as well as the maintenance of the protocol.
