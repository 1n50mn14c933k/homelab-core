# Security Policy

## Scope

This repository contains sanitized homelab documentation and examples.

Do not submit:

* Real passwords
* API tokens
* SSH private keys
* VPN keys
* Public/private key material
* Internal IP maps
* Firewall exports
* Backup repository credentials
* Customer or third-party data

## Reporting a Security Issue

If you find a security issue in this repository, please open a private security advisory or contact the repository owner through GitHub.

## Secret Handling

Secrets must never be committed to this repository.

Use:

* `.env.example` for example variables
* GitHub repository secrets for CI/CD secrets
* Password manager entries for real credentials
* Private repositories for sensitive lab inventory

## Before Every Change

1. Check backup/snapshot status
2. Open a change request issue
3. Document the expected impact
4. Test rollback steps
5. Merge only after review
