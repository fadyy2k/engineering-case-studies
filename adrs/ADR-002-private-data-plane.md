# ADR-002: Keep Database and Control Traffic Off the Public Internet

**Status:** Accepted

## Decision

Use private connectivity or authenticated overlay networking for database replication and administrative/control traffic whenever the systems can support it.

## Rationale

Reducing public service exposure removes an entire class of Internet-originated probing and simplifies firewall intent. Authentication and authorization are still required; private networking is not treated as a substitute for identity controls.
