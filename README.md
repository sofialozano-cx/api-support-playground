<div align="center">

# API Support Playground

### REST APIs · HTTP · Authentication · Webhooks · Troubleshooting

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

## Interactive Modules

| Module | What it demonstrates |
|---|---|
| **Request Lab** | GET, POST, PATCH and DELETE request construction |
| **Authentication** | Bearer token and API-key failure patterns |
| **Response Inspector** | Status, headers, latency and structured JSON responses |
| **Rate Limits** | 429 responses, remaining quota and retry guidance |
| **Webhooks** | Delivery attempts, receiver responses and retry reasoning |
| **Troubleshooting Challenges** | Evidence-based diagnosis of realistic API support cases |

---

## Troubleshooting Coverage

The lab includes scenarios around:

`200` · `201` · `204` · `400` · `401` · `403` · `404` · `409` · `422` · `429` · `500`

The objective is not memorizing status codes. Each scenario asks a support-oriented question: **what does the evidence tell us, what should we verify next, and is the likely owner the customer, Support, or Engineering?**

---

## Support Workflow

```text
Customer symptom
      ↓
Inspect request
      ↓
Check auth + headers + payload
      ↓
Read status + response body
      ↓
Separate client-side from platform-side hypotheses
      ↓
Test / gather evidence
      ↓
Resolve or escalate with context
```

---

## Portfolio Context

This project complements my **Technical Support Lab**. That repository emphasizes structured written investigations; this application makes the underlying HTTP, API, authentication, rate-limit and webhook concepts interactive.

It is a portfolio simulation and is not presented as production API-support experience from a previous employer.

---

<div align="center">

### Sofia Lozano
Customer Experience · Technical Support · CRM & Support Operations

[GitHub Profile](https://github.com/sofialozano-cx)

</div>
