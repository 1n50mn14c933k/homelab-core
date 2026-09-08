# Security Policy

## Scope

This repository contains **sanitized public homelab documentation and examples**. Everything committed here should be assumed publicly accessible.

## Never Commit

Do not commit:

- Real passwords, recovery codes, or API tokens
- SSH/VPN/TLS private keys
- Code-signing private keys or certificates
- Real `.env` files
- Internal IP maps
- Sensitive hostnames or usernames
- Firewall/router exports
- Private DNS zone data
- Backup repository credentials
- Serial numbers or asset identifiers
- Customer or third-party data
- Raw logs/screenshots containing sensitive information

## Reporting a Security Issue

Do **not** publish exploitable findings or exposed credentials in a public issue.

Use GitHub private security reporting/security advisories when available, or contact the repository owner privately through GitHub.

## Secret Handling

Use:

- `.env.example` for non-secret variables
- GitHub repository secrets for CI/CD values
- A password manager for operational credentials
- `private-lab-inventory` for sensitive inventory
- Dedicated secure storage for private keys and certificates

If a credential is accidentally committed, assume compromise and revoke/rotate it immediately. Removing it only from the newest commit is not sufficient.

## Public Documentation Standard

Before publishing:

1. Replace real addressing with documentation networks
2. Remove real hostnames, usernames, domains, and admin endpoints
3. Remove serial numbers and hardware identifiers
4. Remove credentials, tokens, certificates, and private keys
5. Sanitize screenshots and logs
6. Verify exports do not contain embedded secrets
7. Avoid exposing operational attack surface without educational value

## GitHub Actions

Workflows should use least privilege, pin third-party actions where practical, avoid unnecessary write permissions, never echo secrets, and never upload sensitive inventory as artifacts.
