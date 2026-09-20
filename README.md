# Engineering Case Studies

[![Repository Guard](https://github.com/fadyy2k/engineering-case-studies/actions/workflows/repository-guard.yml/badge.svg)](https://github.com/fadyy2k/engineering-case-studies/actions/workflows/repository-guard.yml)

Sanitized engineering write-ups focused on **architecture, operational trade-offs, rollback, reliability, security boundaries, and lessons learned** from production-style infrastructure work.

These are not deployable copies of private systems. Names, credentials, IP plans, internal DNS, customer data, exact firewall rules, administrative endpoints, and proprietary source are intentionally omitted or generalized.

## Case studies

| Case study | Engineering focus |
| --- | --- |
| [Multi-tenant SaaS platform](case-studies/01-multi-tenant-saas-platform.md) | isolation, deployment, backups, observability, capacity |
| [Cross-site PostgreSQL replication](case-studies/02-cross-site-postgresql-replication.md) | private connectivity, logical replication, rollback, lag |
| [Cloud migration with rollback](case-studies/03-cloud-migration-with-rollback.md) | replication-first cutover, DNS, validation, failback |
| [Observability baseline](case-studies/04-observability-baseline.md) | metrics, symptoms, alerts, runbooks |
| [Identity and workspace hardening](case-studies/05-identity-security-hardening.md) | MFA, mail authentication, sharing, DLP, rollout |
| [Local-first internal AI platform](case-studies/06-local-first-ai-platform.md) | data boundaries, RAG, RBAC, plugin/network risk |

## Engineering decisions

- [ADR-001 — Treat rollback as a first-class release feature](adrs/ADR-001-rollback-first.md)
- [ADR-002 — Keep database/control traffic off the public Internet](adrs/ADR-002-private-data-plane.md)
- [ADR-003 — Separate public evidence from private operational detail](adrs/ADR-003-public-evidence-boundary.md)

## How to read these

Each case study uses the same structure:

```text
Problem → Constraints → Architecture → Failure modes → Controls → Validation → Lessons
```

The goal is not to present perfect systems. It is to document **why a design was chosen, what could fail, how failure was detected, and how rollback/recovery was planned**.

## Related public implementations

- [AWS EKS Platform Engineering reference](https://github.com/fadyy2k/platform-engineering-eks-gitops)
- [MIND DevSecOps reference](https://github.com/fadyy2k/depi-mind-app-v2)
- [AWS EKS Terraform reference](https://github.com/fadyy2k/depi-helloapp-infra-v2)
- [Multi-EC2 Ansible automation](https://github.com/fadyy2k/notesapp-multi-ec2-ansible)
- [Engineering portfolio](https://fadyy2k.github.io/portfolio/)

## Publication boundary

See [SANITIZATION.md](SANITIZATION.md). If a write-up would expose a real environment rather than teach a reusable engineering pattern, it stays private.
