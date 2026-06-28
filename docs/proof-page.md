# Proof Page

The Proof Page is the first user-facing product built on top of the ChainTrace Protocol.

The goal is simple:

> Help a small business create a verifiable proof page in minutes.

## User Flow

```text
Upload evidence
        ↓
Generate hash
        ↓
Anchor proof on testnet or mainnet
        ↓
Generate public proof page
        ↓
Share link or QR code
        ↓
Anyone can verify the proof
```

## Supported Proof Types

Initial proof types:

- product proof
- shipment proof
- invoice proof
- inspection proof
- delivery proof
- buyer acceptance proof

## Proof Page Fields

A proof page may show:

- proof title
- proof type
- batch ID
- file hash
- URI or CID
- submitter address
- timestamp
- blockchain transaction hash
- related events
- related attestations
- QR code
- verification button

## Viral Loop

Each proof page should include:

> Create your own proof

This turns every public proof page into an acquisition surface.

A small business shares the proof page with a buyer, logistics partner, financier, or customer. The viewer can verify the record and create their own proof.

## Design Principle

The proof page should not feel like a complex crypto application.

It should feel like:

- a trust page
- a public receipt
- a business proof card
- a QR-verifiable evidence page

## First MVP Goal

A user should be able to create a proof page in under three minutes.

Minimum MVP features:

- file upload
- SHA-256 hash generation
- simple metadata form
- wallet connection
- testnet anchoring
- proof page generation
- QR code generation
- proof verification
