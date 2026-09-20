# ADR-001: Treat Rollback as a First-class Release Feature

**Status:** Accepted

## Decision

Every production change pattern documented here must identify a reversible path before the change is executed.

## Rationale

Recovery under incident pressure is slower and riskier when rollback logic is invented after failure. DNS changes, application releases, database migrations and infrastructure cutovers all need explicit reversal criteria and state assumptions.

## Consequence

A release is not considered fully automated merely because deployment is automated. The release process must also expose the known-good version/state and the steps required to return to it.
