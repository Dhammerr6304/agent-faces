# Inference Receipts and the ICE Pipeline

## Pipeline Overview

```
Human Face
    ↓
Agent Face
    ↓
Inference Receipts (IR)
    ↓
ICE Ledger (Immutable Chain Evidence)
```

## Purpose

- Humans consume stories and interfaces.
- Agents consume structured evidence.
- ICE records what was actually observed and acted upon, outside the mutable control of any single party.

## Inference Receipts

An Inference Receipt is a signed, hash-chained record of a specific agent interaction with an Agent Face. Minimum useful fields typically include:

- Agent identity / principal
- Timestamp
- Target surface (URL or endpoint)
- What was retrieved or invoked
- Outcome / result summary
- Previous receipt hash (for chaining)
- Cryptographic signature

Exact schema work is ongoing and will live under `/schemas`.

## ICE Ledger

The Immutable Chain Evidence layer anchors the chain of receipts (or their hashes) to a durable, independently verifiable substrate. This may be a public blockchain, a specialized evidence network, or any system that provides strong immutability and public verifiability guarantees.

The goal is independent auditability of agent observations and actions, not merely internal logging.
