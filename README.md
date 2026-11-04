# Aegis Guard

**Risk-aware governance for LLM-based cyber incident response.**

Aegis Guard is a sandboxed platform where an LLM investigates simulated cyber incidents
and proposes response actions, while an independent deterministic policy engine decides
whether each action may execute automatically or requires human approval.

## Core principle

> The LLM investigates and proposes. The policy engine authorizes.

Model confidence is not authorization.

## Problem

LLM agents can read incident evidence and propose actions such as disabling an account,
isolating a host, or blocking an IP. However, untrusted evidence can contain indirect
prompt-injection instructions, and a confident model can still be wrong.

## What we are building

- Reproducible simulated incident scenarios
- A sandboxed execution environment
- Evidence with trusted/untrusted provenance
- An LLM investigation agent with narrow read-only tools
- A deterministic risk and policy engine
- Human approval for high-impact actions
- A complete audit trail
- A dashboard showing the authorization boundary in real time

## Status

🚧 Under active development.

## Tech stack

- Python
- FastAPI
- Pydantic
- PostgreSQL
- React / Next.js
- pytest

## Safety boundary

This project does not interact with real infrastructure. All hosts, accounts, alerts,
and response actions exist only inside a simulated environment.
