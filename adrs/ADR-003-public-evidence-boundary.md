# ADR-003: Separate Public Engineering Evidence from Private Operational Detail

**Status:** Accepted

## Decision

Publish architecture patterns, trade-offs, sanitized metrics, test strategies and rollback decisions. Keep environment-identifying operational detail private.

## Rationale

A public engineering portfolio should provide enough evidence for another engineer to evaluate the design without exposing a real production attack surface.
