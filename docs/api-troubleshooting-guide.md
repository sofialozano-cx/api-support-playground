# API Troubleshooting Guide

## Purpose

A compact support workflow for investigating fictional RelayDesk API reports in this portfolio lab.

## 1. Capture the Symptom

Record the HTTP method, endpoint, approximate timestamp, status code, request/error ID and expected versus actual behavior. Ask for sanitized evidence; do not request full API secrets.

## 2. Authentication vs. Authorization

- **401**: verify whether credentials are present, correctly formatted, current and valid for the environment.
- **403**: credentials may be valid while the caller lacks the required role or scope.

## 3. Request Construction

Check method, resource path, Content-Type, required fields and JSON syntax. Separate malformed requests (often 400) from syntactically valid payloads that fail field/business validation (often 422 in this simulated API).

## 4. Resource State

For 404 or 409 responses, verify identifiers and current resource state before assuming platform failure.

## 5. Rate Limits

For 429 responses, inspect rate-limit headers and Retry-After. Recommend appropriate pacing/backoff rather than immediate repeated retries.

## 6. Server Errors

A single 5xx is not enough to define incident scope. Gather request IDs, timestamps and reproduction evidence. Correlated failures across independent accounts with unchanged previously healthy requests strengthen a platform-side hypothesis and should trigger Engineering/incident assessment.

## 7. Escalation Package

A useful escalation includes impact, expected/actual behavior, safe identifiers, timestamps, status/response evidence, troubleshooting already completed, reproduction scope and a clear question for Engineering.

> Status-code conventions vary by API. The behavior documented here describes the fictional RelayDesk simulation and should not be treated as a universal contract for every API.
