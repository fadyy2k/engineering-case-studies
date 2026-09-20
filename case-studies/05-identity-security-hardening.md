# Identity and Workspace Security Hardening

## Problem

Raise collaboration/identity security controls without causing unmanaged user lockouts or mail-delivery failures.

## Control areas

- MFA enforcement
- SPF / DKIM / DMARC validation
- reduced external sharing
- data-loss controls for sensitive data classes
- administrative-role review
- exception tracking and break-glass planning

## Rollout approach

```text
inventory → communicate → pilot → enforce → verify → monitor exceptions
```

Security settings were treated as a rollout program rather than a collection of toggles. Mail-security changes were validated after DNS publication, and identity enforcement included a recovery path for legitimate lockouts.

## Lesson

A stronger security policy that operators cannot recover from safely creates a different operational risk. **Enforcement and recovery design belong together.**
