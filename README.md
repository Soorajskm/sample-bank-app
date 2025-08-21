CozyCredit — Sample Banking App
CozyCredit is a modern, secure, and developer-friendly sample banking application. It demonstrates best practices for building a fintech-grade system across authentication, accounts, payments, cards, and notifications with a clean modular architecture. This repository is intended for learning, prototyping, and architectural reference—not for production banking use without rigorous compliance, audits, and certifications.

Features
Secure onboarding with email/phone verification and optional eKYC stub

OAuth2/OIDC auth with MFA simulation and biometric unlock on mobile

Accounts: balances, transactions with categories, statements (mock PDFs)

Payments: internal transfers, scheduled/recurring, payee management

Cards: virtual card issuance, freeze/unfreeze, spend limits

Notifications: push/email/SMS via pluggable providers (dev-friendly console sink)

Support inbox: secure messages, dispute initiation flow

Admin console: user search, risk flags, rate limits, feature flags

Observability: structured logs, metrics, traces; request correlation

Tech Stack
Backend: Node.js (NestJS) or Python (FastAPI) variants selectable via template

Auth: OAuth2/OIDC (PKCE), JWT access/refresh, short-lived tokens

DB: PostgreSQL (primary), Redis (cache/rate limits), MinIO/S3 (documents)

Messaging: Kafka (events), BullMQ/Celery (jobs)

Mobile: React Native (Expo) with platform biometrics; Web: Next.js

Infra: Docker Compose (local), Terraform modules (optional), GitHub Actions CI

Testing: Jest/PyTest, Playwright (E2E), k6 (load), Semgrep (SAST)

Repository Structure
/apps

/api — REST/GraphQL API, domain services, adapters

/web — Next.js web client (CSR/SSR mix)

/mobile — React Native app (Expo)

/admin — Admin/ops console

/packages

/domain — Shared domain models and validations

/auth — OIDC provider setup and client SDK

/ui — Component library (web/mobile)

/observability — Logging/metrics/tracing helpers
