<div align="center">

# API Support Playground

### REST APIs · HTTP · Authentication · Webhooks · Troubleshooting

**[→ Open Live Playground](https://api-support-playground.vercel.app/)**

![Status](https://img.shields.io/badge/Status-Live-22C55E?style=flat-square)
![React](https://img.shields.io/badge/Frontend-React-4F46E5?style=flat-square)
![TypeScript](https://img.shields.io/badge/Language-TypeScript-6D28D9?style=flat-square)
![API](https://img.shields.io/badge/Focus-API%20Support-7C3AED?style=flat-square)
![Simulation](https://img.shields.io/badge/Environment-Simulated-8B5CF6?style=flat-square)

</div>

---

## Overview

API Support Playground is an interactive portfolio lab for **technical support reasoning around REST APIs**. It simulates the kind of evidence a support professional may inspect when a customer reports an integration problem: method, endpoint, authentication, headers, JSON payload, HTTP response, rate-limit metadata and webhook delivery behavior.

The fictional API belongs to **RelayDesk**, a simulated B2B SaaS product used elsewhere in this portfolio. No external production API, customer account, secret or employer data is used.

> Requests are evaluated by a deterministic in-browser simulation. The application is designed to demonstrate HTTP/API concepts and troubleshooting logic, not to impersonate access to a production backend.

---

## Live Playground

**Live application:** https://api-support-playground.vercel.app/

The interface is organized into five support-focused modules:

| View | Support question |
|---|---|
| **Request Lab** | Is the request constructed correctly and what does the response evidence show? |
| **Auth** | Is this an authentication problem (401) or an authorization problem (403)? |
| **Rate Limits** | Is the client hitting a quota and how should retries be handled? |
| **Webhooks** | Where did an event fail across creation, delivery and receiver response? |
| **Challenges** | Can the available evidence support a defensible diagnosis and next step? |

---

## Interactive Request Lab

The simulated API explorer supports:

- `GET /v1/customers/:id`
- `POST /v1/customers`
- `PATCH /v1/customers/:id`
- `DELETE /v1/customers/:id`
- `POST /v1/webhooks/test`

The Request Lab exposes request method, endpoint, Bearer authentication, JSON body, response status, response headers, latency and structured JSON output. Deliberate input changes produce deterministic failure states for investigation.

Examples include clearing credentials to inspect a `401`, using a revoked/expired-token simulation, sending malformed JSON for `400`, and sending a semantically invalid customer payload for `422`.

---

## Troubleshooting Challenges

Six interactive cases test evidence-based support reasoning:

| Case | Signal | Core diagnosis |
|---|---:|---|
| Token rejected after key rotation | `401` | Integration still using revoked credentials |
| Valid token, forbidden action | `403` | Authentication succeeds but required scope is missing |
| Customer ID cannot be found | `404` | Incorrect resource identifier |
| Valid JSON fails validation | `422` | Payload semantics violate field requirements |
| Burst traffic starts failing | `429` | Request quota exhausted |
| Same request fails across accounts | `500` | Correlated evidence supports a platform-side hypothesis |

Each challenge includes evidence, multiple diagnoses, feedback, recommended next step and likely ownership. The goal is to distinguish **customer configuration, Support guidance and Engineering/incident escalation** rather than simply memorize HTTP codes.

---

## Support Workflow

```text
Customer symptom
      ↓
Inspect method + endpoint
      ↓
Check authentication / authorization
      ↓
Validate headers + JSON payload
      ↓
Read status + response body + request ID
      ↓
Separate client-side from platform-side hypotheses
      ↓
Test / gather correlated evidence
      ↓
Resolve, guide, or escalate with context
```

---

## Concepts Demonstrated

`REST APIs` · `HTTP Methods` · `JSON` · `Bearer Authentication` · `Authorization Scopes` · `Request IDs` · `Status Codes` · `Rate Limits` · `Retry-After` · `Webhooks` · `Troubleshooting` · `Engineering Escalation`

### Status Coverage

`200` · `201` · `204` · `400` · `401` · `403` · `404` · `422` · `429` · `500`

Status-code behavior can differ across real APIs. The scenarios in this repository describe the fictional RelayDesk contract and are not presented as universal API behavior.

---

## Technical Architecture

```text
React + TypeScript
       ↓
Interactive support console
       ↓
Deterministic browser-side API simulator
       ↓
Synthetic request / response evidence
       ↓
Troubleshooting challenges + support reasoning
```

**Stack:** React · TypeScript · Vite · CSS

There are intentionally no production credentials or external API dependencies in the simulation.

---

## Documentation

- [`docs/api-troubleshooting-guide.md`](docs/api-troubleshooting-guide.md) — compact investigation workflow covering authentication, authorization, request construction, resource state, rate limits, server errors and Engineering escalation.

---

## Portfolio Context

This project complements my **Technical Support Lab**. That repository emphasizes structured written investigations; this application makes the underlying HTTP, API, authentication, rate-limit and webhook concepts interactive.

Together they demonstrate both sides of technical support practice: **reasoning/documentation and hands-on interpretation of technical evidence**.

This is a portfolio simulation and is not presented as production API-support experience from a previous employer.

---

<div align="center">

### Sofia Lozano
Customer Experience · Technical Support · CRM & Support Operations

**[Live Playground](https://api-support-playground.vercel.app/)** · **[GitHub Profile](https://github.com/sofialozano-cx)**

</div>
