# Youssef El Mounabih

Applied AI engineer. I build agentic systems and the infrastructure that keeps
them honest: signed audit trails, database-enforced invariants, real tests.
Fully remote, B2B through a US LLC.

## even: the receipt layer for AI agents

**Live demo: [even-receipts.vercel.app](https://even-receipts.vercel.app)** ·
[github.com/SpowZy/even](https://github.com/SpowZy/even)

Every action an AI agent takes produces a signed, hash-chained receipt:
per-action cost, policy verdicts, and proof auditors can re-verify. Tamper
with one byte and verification names the exact broken link.

- sha256 hash chain + ed25519 signatures per run, zero crypto dependencies
- Append-only stores, including Postgres with a trigger that rejects UPDATE/DELETE
- Policy guardrails: budget hard-stops, blocked tools, PII redaction before persistence
- 52 unit tests + 13 Playwright e2e covering forgery, replay, crash-resume and tampering

## Open source

Two merged PRs into [Floe-Labs/floe-guard](https://github.com/Floe-Labs/floe-guard/pulls?q=is%3Apr+author%3ASpowZy),
a billing guardrail for AI agents:

- LangGraph adapter with atomic fan-out reserve/settle and typed budget advisory
- Anthropic cache-aware pricing

## Selected projects

| project | what it proves |
| --- | --- |
| [swellbook](https://github.com/SpowZy/swellbook) | Booking platform where double-booking is physically impossible: PostgreSQL exclusion constraint, idempotent writes, 25-way race test with exactly one winner. [Live](https://swellbook.vercel.app) |
| [taskrank](https://github.com/SpowZy/taskrank) | Multi-objective marketplace ranking engine balancing revenue, conversion and new-provider cold-start |
| [streamcap](https://github.com/SpowZy/streamcap) | Local-first system-audio captions with sub-second latency and cost-aware hybrid cloud routing |
| [beacon](https://github.com/SpowZy/beacon) | Privacy-first agentic router for hyperlocal community alerts |

## How I work

Typed contracts before code. Invariants enforced at the lowest layer that can
hold them: database, cryptography, types. Tests that simulate the failure, not
the happy path. Docs a skeptical staff engineer can audit: architecture,
threat model, failure analysis.

Contact: elmounabih.youssef@gmail.com

