# ChainTrace Data Model

ChainTrace starts with a minimal data model.

The goal is not to model every possible supply chain workflow. The goal is to define a small set of objects that can support many workflows through open composition.

## 1. Proof

A proof anchors evidence to a hash, URI, timestamp, and submitter.

Example:

```json
{
  "proofType": "invoice",
  "fileHash": "0x...",
  "uri": "ipfs://...",
  "submitter": "0x...",
  "timestamp": 1780000000,
  "metadataHash": "0x..."
}
```

A proof can represent:

- product image
- invoice
- contract
- quality inspection report
- shipping document
- warehouse receipt
- delivery confirmation

## 2. Batch

A batch represents a product batch, shipment, order, or trade object.

Example:

```json
{
  "batchId": "COFFEE-VN-2026-0001",
  "name": "Vietnam Coffee Beans Batch 0001",
  "creator": "0x...",
  "metadataHash": "0x..."
}
```

Batch is intentionally flexible. A user can map it to a physical product, shipment, order, invoice group, or trade deal.

## 3. Artifact

An artifact is a file, image, report, invoice, certificate, video, or other evidence object.

An artifact may be stored on IPFS, Arweave, cloud storage, enterprise storage, or local storage.

ChainTrace only needs a verifiable reference:

- hash
- URI or CID
- submitter
- timestamp
- optional metadata hash

## 4. Event

An event records something that happened in the supply chain.

Initial event types:

- CREATED
- PRODUCED
- INSPECTED
- SHIPPED
- STORED
- DELIVERED
- ACCEPTED
- REJECTED

Example:

```json
{
  "batchId": "COFFEE-VN-2026-0001",
  "eventType": "INSPECTED",
  "proofId": 1,
  "actor": "0x...",
  "timestamp": 1780000000,
  "metadataHash": "0x..."
}
```

Custom event types should be allowed as the ecosystem grows.

## 5. Attestation

An attestation is a signed statement made by an actor about a proof, batch, event, receivable, or business passport.

Example:

```json
{
  "schema": "quality_report_v1",
  "subject": "COFFEE-VN-2026-0001",
  "claimHash": "0x...",
  "issuer": "0x...",
  "evidenceProofId": 1,
  "signature": "0x..."
}
```

Attestations can be used by:

- quality inspectors
- buyers
- logistics providers
- financiers
- auditors
- AI agents

## 6. Receivable Proof Pack

A receivable proof pack links trade evidence into a financing-ready evidence bundle.

It may include:

- order proof
- invoice proof
- shipment proof
- delivery proof
- buyer acceptance
- risk summary
- related attestations

ChainTrace should not directly become a lender in the early stage. The protocol prepares verifiable evidence for financing partners.

## 7. Business Passport

A business passport is a public or selectively shared profile built from proofs, events, and attestations.

It can show:

- verified product proofs
- shipment history
- invoice history
- buyer confirmations
- dispute records
- AI-generated summaries
- public verification links

The purpose is to help small businesses build portable, verifiable trade reputation.
