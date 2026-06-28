# AI Agent Layer

ChainTrace is designed to be used by humans, companies, existing platforms, and AI agents.

AI agents can process information, but they need verifiable facts. ChainTrace provides the shared fact layer that agents can read, verify, and extend.

## Why AI Agents Need ChainTrace

AI agents can:

- read documents
- summarize invoices
- compare logistics records
- detect missing steps
- generate risk reports
- coordinate workflows

But AI agents still need to know:

- whether a file was changed
- who submitted an event
- when a record was anchored
- whether a buyer accepted delivery
- whether an invoice is linked to real trade evidence
- whether a claim was signed by a known actor

ChainTrace provides the verifiable memory layer for these tasks.

## Official Agent Concepts

### 1. Evidence Agent

The Evidence Agent helps users turn files into verifiable proofs.

It can:

- classify files
- extract basic metadata
- calculate hashes
- suggest proof type
- prepare metadata
- submit proof requests
- generate public proof descriptions

### 2. Trace Agent

The Trace Agent organizes supply chain events.

It can:

- read all events linked to a batch
- generate a timeline
- detect missing events
- summarize product journey
- prepare public trace pages

### 3. Finance Pack Agent

The Finance Pack Agent prepares financing evidence bundles.

It can:

- collect order, invoice, shipment, delivery, and acceptance proofs
- generate a receivable proof pack
- flag missing buyer confirmation
- summarize risk factors
- prepare a financier review view

### 4. Compliance Agent

The Compliance Agent helps keep the protocol within safe boundaries.

It can:

- flag restricted jurisdictions
- warn against investment-return language
- check whether a workflow may involve lending, securities, payment, or stablecoin issues
- suggest KYC/KYB checkpoints
- distinguish proof infrastructure from financial services

### 5. Integration Agent

The Integration Agent helps existing systems connect to ChainTrace.

It can:

- map ERP/SaaS fields to ChainTrace objects
- generate API examples
- produce SDK snippets
- validate schema compatibility
- prepare sample integration plans

## Third-party Agent Compatibility

Third-party agents should be able to declare:

- agent name
- operator address
- supported schemas
- public key
- service endpoint
- capability description
- risk level

Example:

```json
{
  "agentName": "LogisticsRiskAgent",
  "agentType": "risk_analysis",
  "operator": "0x...",
  "supportedSchemas": [
    "proof_v1",
    "batch_v1",
    "event_v1",
    "receivable_pack_v1"
  ],
  "publicKey": "0x...",
  "serviceEndpoint": "https://example.com/agent"
}
```

## Boundary

ChainTrace should not control every agent.

It should define the minimum boundary:

- signed identity
- declared capability
- supported schema
- verifiable output
- traceable action
- optional reputation and staking model

Within that boundary, the ecosystem can grow its own order.
