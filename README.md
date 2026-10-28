# Paul Osorio Schuler

Backend engineer · TypeScript and Node.js · Lima, Peru (UTC-5)

Fifteen years building backend systems, most of them spent making systems that were never designed
together behave as one. Today I design, build and run a product of my own, end to end.

I write down why. Most of what I have to show is in those notes.

---

## Now

**[Chekalo](https://chekalo.pe)** — price intelligence for Peruvian retail. It ingests nine
retailers daily, resolves the same product across stores into one canonical identity, and keeps
every seller's price history so a discount can be checked instead of trusted.

- **Modular monolith.** Ingestion, catalog and search projection, each owning its own state behind a
  hard boundary. One deployable.
- **Deterministic identity resolution.** Brand, model and variant signature, corroborated by barcode.
  It replaced an embeddings and LLM approach that worked, but was not reproducible, auditable or
  cheap.
- **Ingestion that expects to be interrupted.** Redis and BullMQ, per-retailer rate limits and
  retries, every payload validated at the boundary.
- **Search as a projection.** PostgreSQL holds the truth; only what changed goes to OpenSearch,
  reindexed behind alias swaps. The site is a read model: React Router with SSR, no API of its own.
- **Decisions on record.** Over a hundred ADRs in the pipeline alone.

## Before

A decade designing and delivering enterprise integration and orchestration platforms: workflow
engines over message brokers, workers in .NET and Python, legacy cores behind modern web layers.
Led teams of up to 22 engineers, set the engineering standards they worked under, and wrote the code
myself when a deadline required it.

---

## Code

| | |
| --- | --- |
| [`url-shortener`](https://github.com/poschuler/url-shortener) | Fastify, hexagonal architecture, separate write and read APIs, load-tested |
| [`nodejs-result-pattern`](https://github.com/poschuler/nodejs-result-pattern) | Expected failures returned as values; exceptions kept for what is truly unexpected |
| [`nodejs-ddd-value-objects`](https://github.com/poschuler/nodejs-ddd-value-objects) | Value objects in TypeScript: self-validating, immutable, compared by value |
| [`pragmatic-nodejs-api`](https://github.com/poschuler/pragmatic-nodejs-api) | Express API with vertical slices, Zod validation and centralized error handling |
| [`poschuler.com`](https://github.com/poschuler/poschuler.com) | Markdown in git, derived into D1 and KV at build time, served from a Cloudflare Worker |

## Writing

- [Designing a URL shortener](https://poschuler.com/blog/designing-a-url-shortener)
- [Implementing the Result pattern in Node.js](https://poschuler.com/blog/implementing-the-result-pattern-in-nodejs)
- [Implementing Value Objects in Node.js](https://poschuler.com/blog/implementing-value-objects-in-nodejs)
- [Pragmatic Node.js API](https://poschuler.com/series/pragmatic-nodejs-api) — a three-part series

## How I work

- **Boundaries before services.** A modular monolith until a split earns its cost.
- **Written decisions.** ADRs, a domain glossary and an `AGENTS.md` in every repository.
- **Coding agents, daily.** Fully specified issues run headless in isolated worktrees, with a human
  gate before anything merges. The leverage is in what the repository tells the agent, not in the
  model.

## Stack

**Backend** — TypeScript, Node.js, Express, Fastify, BullMQ, Kysely, Zod, Vitest\
**Data** — PostgreSQL, OpenSearch, Redis, SQL Server\
**Infrastructure** — Google Cloud, Cloudflare Workers, Docker, GitHub Actions, Linux\
**Integration** — Kafka, Camunda, .NET, Python\
**Frontend** — React, React Router, Tailwind CSS\
**Architecture** — Domain-driven design, modular monoliths, hexagonal architecture, vertical slices, event-driven integration

iSAQB® CPSA-F · Azure Developer Associate · MBA · B.S. in Software Engineering

---

[poschuler.com](https://poschuler.com) · [CV](https://poschuler.com/cv) · [LinkedIn](https://www.linkedin.com/in/poschuler) · [poschuler@gmail.com](mailto:poschuler@gmail.com)
