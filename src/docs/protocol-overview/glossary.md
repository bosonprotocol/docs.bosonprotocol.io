---
layout: docs
title: "Boson Protocol: Docs: Protocol Overview: Glossary"
short_title: "Glossary"
permalink: /protocol-overview/glossary/
---

# Glossary

- **Seller**: User of the app/protocol who has an asset they wish to sell.
- **Buyer**: User of the app/protocol who has an asset they wish to buy.
- **Voucher**: The representation of a Thing that has been offered by a seller
  and committed to by a buyer. A voucher is not created within a voucher set
  unless a buyer has committed to it. This is sometimes also referred to as:
  Order and NFTV in parts of the system.
- **Voucher Set**: A set or collection of things that have been offered for sale
  by a seller. It can have a quantity greater than or equal to 1. This is
  sometimes also referred to as: Voucher Supply; Token Supply; Offer; Listing
- **Voucher Lifecycle**: The series of steps and states through which a voucher
  passes from when it is first committed to when it is final. A voucher may have
  more than one state at a time.
- **Offer**: An action in the exchange mechanism in which a seller 'offers' a
  voucher set for commitment and redemption by a buyer. As part of this action,
  a deposit, known as the seller deposit, is put into escrow. If there are
  multiple items within a voucher set the total seller deposit is mutliplied by
  the quantity.
- **Commit**: An action in the exchange mechanism in which a buyer 'commits'
  their intention to purchase an asset. As part of this action a deposit, known
  as the buyer deposit, is put into escrow.
- **Redeem**: An action in the exchange mechanism in which a buyer acknowledges
  receipt of the asset. This redemption must be done after the start date but
  before the expiry date of the voucher set (also known as the voucher validity
  period).
- **Refund**: An action in the exchange mechanism in which a buyer chooses to
  receive a refund for the voucher. In doing so they will receive their payment
  back, but potentially lose their deposit.
- **Complain**: An action in the exchange mechanism in which a buyer chooses to
  complain about a voucher, signaling the dissatisfaciton of the promise
  execution. In doing so the Seller may get penalized.
- **Cancel or Fault**: An action in the exchange mechanism in which a seller
  'offers' can cancel or fault a particular voucher. This will cancel the
  current offer and corresponding voucher, and all or part of the buyers deposit
  will be refunded along with the payment amount.
- **Void**: An action in which a seller may void all remaining uncommitted
  assets within a voucher set. This has no effect on committed or finalised
  vouchers.
- **Finalise**: An automated action in the exchange mechanism in which a voucher
  can no longer be used. This is triggered once all wait periods are passed.
- **Escrow**: A place of custody or trust until a specified condition has been
  fulfilled.
- **Order**: See Voucher
- **Security Deposit**: A configurable amount that is put into escrow by a user
  (buyer or seller) to place a stake in the exchange to facilitate trust.
- **Wait period**: Periods designed in the game tree which allow time for one or
  more parties to act. These are either configured by a user or set as default
  by the system admin.
- **Voucher validity period**: A wait period defined by the seller at the
  creation of the voucher set. It is the period between the start date and the
  end date in which a voucher from a vocuher set can be redeemed.
- **Complain period**: A wait period defined by the admin for a time period in
  which a buyer can complain upon redemption.
- **Cancel or fault period**: A wait period defined by the admin for a time
  period in which a seller can issue a cancel or fault transaction.
- **Price**: The price of the asset which is payable from the buyer to the
  seller on commitment.
- **Currency**: The currency of the transaction (which can be either the price
  or the deposit). The smart contracts currently supports both ETH and $BOSON.
- **Non-fungible token voucher**: See **Voucher**
- **Token Supply**: See **Voucher Set**
- **Voucher Supply**: See **Voucher Set**
- **Listing**: See **Voucher Set**
- **My Vouchers**: A view within the app that lists all the vouchers committed
  to by the wallet of a particular buyer. This voucher set can be filtered by
  Active or Inactive.
- **My Offers**: A view within the app that lists all the voucher sets created
  by the wallet of a particular seller. This voucher set can be filtered by Open
  or Closed.
- **Active Voucher**: The position a voucher is in once it has been committed to
  by a buyer and is yet to be finalised. During this time either a buyer or
  seller has the ability to action it based on the rules of the game tree.
- **Inactive Voucher**: The position a voucher is in once it is finalized (at
  the end of the lifecycle) and can no longer be used.
- **Open Voucher Set**: The position a voucher set is in when either voucher set
  validity period is not expired (before the end date) and/or there is a voucher
  from the voucher set which has not yet been finalised.
- **Closed Voucher Set**: The position a voucher set is in when the voucher set
  validity period is expired (after the expiry date) and all voucher from the
  voucher set are finalized.
- **Asset**: An entity-controlled resource that can potentially create future
  value.
- **Arbitration**: A mechanism for resolving disputes between parties involved
  in a transaction.
- **Non-fungible tokens**: A token that is non-devisble and has a unique
  identifier.
- **Keepers**: For keepers we use
  [Ryan Zurrer's definition](https://rzurrer.medium.com/keepers-workers-that-maintain-blockchain-networks-a40182615b66):"a
  catchall term for the different utility players in distributed network that
  maintain stability and perfrom crucial jobs in the crypto-economic model" To
  find out more about different actors in Boson Protocol refer to our
  Whitepaper.
- **Wallet**: Software that allows users to interact with the smart contracts of
  their desired blockchain.
- **ERC-20**: A smart contract standard for (fungible) tokens,
  [see here](https://eips.ethereum.org/EIPS/eip-20)
- **ERC-1155**: A smart contract standard for managing multiple types of tokens
  (fungible, non-fungible, semi-fungible),
  [see here](https://eips.ethereum.org/EIPS/eip-1155)
- **ERC-721**: A smart contract standard for non-fungible tokens,
  [see here](https://eips.ethereum.org/EIPS/eip-721)
