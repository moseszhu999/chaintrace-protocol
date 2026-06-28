# Protocol Overview

ChainTrace is an open supply chain fact protocol.

It is designed to let small businesses, existing platforms, enterprise systems, and AI agents anchor critical supply chain facts on-chain without replacing their existing workflows.

## What ChainTrace Is

ChainTrace is:

- a fact layer
- a proof layer
- an attestation layer
- an AI-agent-ready coordination layer

It is not:

- a traditional ERP system
- a centralized supply chain SaaS
- a public token sale platform
- a lending platform
- a promise of investment returns

## Minimal Fact Model

A ChainTrace record answers five questions:

1. What happened?
2. Who submitted or signed it?
3. What evidence supports it?
4. When was it anchored?
5. How can another party verify it later?

## Protocol Layers

```text
Physical supply chains
        ↓
Existing ERP / SaaS / logistics / finance systems
        ↓
ChainTrace open fact layer
        ↓
AI agents, proof pages, business passports, finance evidence packs
```

## Core Flow

```text
Upload evidence
        ↓
Generate hash
        ↓
Store file off-chain or externally
        ↓
Anchor hash, URI/CID, timestamp, and submitter on-chain
        ↓
Generate proof page
        ↓
Allow anyone with permission or the shared link to verify
```

## Off-chain and On-chain Split

ChainTrace should not store sensitive commercial files directly on-chain.

On-chain:

- file hash
- URI or CID
- timestamp
- submitter address
- batch ID
- event type
- attestation reference

Off-chain:

- PDFs
- images
- invoices
- contracts
- inspection reports
- private metadata
- AI summaries

This design supports selective proof rather than total exposure.

## Integration Model

Existing platforms can integrate ChainTrace through:

- direct smart contract calls
- REST API
- SDK
- webhook bridge
- no-code proof page interface
- AI integration agent

## AI Agent Layer

AI agents can use ChainTrace to:

- verify evidence hashes
- summarize trade history
- detect missing supply chain events
- prepare receivable proof packs
- check compliance boundaries
- coordinate with other agents around signed facts

The protocol is designed for humans, companies, systems, and AI agents to share a common fact boundary.
