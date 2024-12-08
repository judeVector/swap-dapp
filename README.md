# Swap DApp

This repository contains a Solana on-chain program, **Swap DApp**, implemented using the Anchor framework. The program facilitates secure token swapping through vault-based token handling and offer management.

## Features

- **Make Offer**:

  - Create a new token swap offer.
  - Lock the offered tokens in a secure vault.

- **Take Offer**:
  - Accept and fulfill an existing token swap offer.
  - Exchange tokens securely between the maker and taker.

## Program Workflow

### 1. Make an Offer

The `MakeOffer` instruction allows a user (maker) to:

- Create a new swap offer with specific token requirements.
- Lock the offered tokens in a vault.

**Key Functions:**

- `send_offered_tokens_to_vault`: Transfers tokens from the maker to the vault.
- `save_offer`: Stores offer details on-chain.

### 2. Take an Offer

The `TakeOffer` instruction allows another user (taker) to:

- Accept and fulfill an existing swap offer.
- Exchange tokens and handle vault operations.

**Key Functions:**

- `send_wanted_token_to_maker`: Transfers tokens from the taker to the maker.
- `withdraw_and_close_vault`: Withdraws tokens from the vault to the taker and closes the offer.

## Technology Stack

- **Rust**: High-performance programming language for Solana smart contracts.
- **Anchor**: Framework for building efficient and secure Solana programs.
- **Token Program**: SPL token standard for token management.
