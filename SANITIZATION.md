# Sanitization and Publication Boundary

Public engineering evidence should demonstrate decisions and capability without becoming reconnaissance material for a real environment.

## Never publish

- credentials, tokens, keys or usable connection strings
- public/private production IP addresses or complete network plans
- internal DNS names, admin URLs or VPN/control-plane endpoints
- customer or employee data
- exact production firewall rules tied to reachable systems
- proprietary source code or private configuration
- screenshots containing account IDs, tenant IDs, secrets or identifiable customer information

## Safe publication pattern

Use generalized roles and topology:

```text
Internet → reverse proxy → application tier → data tier
```

instead of publishing real hostnames or addresses.

Use outcome ranges or engineering lessons where exact business-sensitive metrics are unnecessary. Preserve enough evidence to explain the design while removing data that identifies the environment.

## Validation before publication

1. search for credentials and private keys
2. search for real domains, IPs, tenant/account identifiers and email addresses
3. review diagrams for hidden labels or screenshots
4. confirm examples use placeholders such as `example.com`
5. verify the write-up still teaches a reusable engineering decision after sanitization
