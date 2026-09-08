# homelab-core

Main documentation hub for my security-focused homelab.

This public repository contains **sanitized documentation, architecture notes, templates, operating procedures, and security practices** for building and maintaining repeatable infrastructure.

## Purpose

The goal is to document infrastructure that is:

- Secure by default
- Easy to rebuild
- Clear during troubleshooting
- Safe to publish publicly
- Useful for learning real-world infrastructure practices
- Recoverable through documented procedures
- Deliberately separated from private inventory and operational secrets

This repository does **not** contain real secrets, credentials, private keys, internal IP maps, firewall exports, private DNS data, real asset inventory, or sensitive infrastructure identifiers.

## Homelab Focus

- Linux administration and server hardening
- Proxmox virtualization, VMs, and LXCs
- Docker and Compose security
- Network segmentation and DNS
- Monitoring, logging, and alerting
- Identity and access management
- Backup and restore testing
- Ansible and Semaphore automation
- Disaster recovery planning
- Infrastructure documentation and change control

## Security Principles

| Principle | How it is applied |
| --- | --- |
| No secrets in Git | Secrets, keys, tokens, credentials, certificates, and recovery codes are never committed |
| Least privilege | Services, users, containers, workflows, and tokens receive only required access |
| Public/private separation | Public examples remain sanitized; real inventory stays private |
| Repeatable builds | Important systems should be reproducible from documentation and automation |
| Backups before changes | Backup or snapshot state is checked before meaningful changes |
| Monitoring before trust | Services should be observable before they are treated as reliable |
| Tested recovery | Backups are not trusted until restore procedures are tested |
| Change control | Meaningful changes are documented, reviewed, and reversible |

## Repository Map

```text
homelab-core/
├── README.md
├── SECURITY.md
├── LICENSE
├── .github/
│   ├── CODEOWNERS
│   ├── dependabot.yml
│   ├── pull_request_template.md
│   ├── ISSUE_TEMPLATE/
│   │   └── change-request.yml
│   └── workflows/
│       └── repository-hygiene.yml
├── docs/
│   ├── 00-overview.md
│   ├── 01-network.md
│   ├── 02-servers.md
│   ├── 03-security.md
│   ├── 04-backups.md
│   ├── 05-disaster-recovery.md
│   └── CHANGE-WORKFLOW.md
├── inventory/
│   ├── hosts.example.yml
│   └── services.example.yml
├── diagrams/
│   └── README.md
└── scripts/
    └── README.md
```

## Public / Private Boundary

This public repository may contain:

- Sanitized documentation
- Example configurations
- Example inventory
- Security checklists
- Backup/recovery procedures
- Diagrams using documentation networks
- Automation examples without credentials or private identifiers

Do **not** commit:

- Passwords, recovery codes, or API tokens
- SSH/VPN/TLS private keys or signing material
- Real `.env` files
- Internal IP maps or sensitive hostnames
- Public administration endpoints
- Firewall/router/DNS exports
- Backup credentials
- Serial numbers or asset identifiers
- Customer or third-party data
- Raw screenshots/logs containing sensitive metadata

Real inventory and operational values belong in the private `private-lab-inventory` repository.

## Change Workflow

This repository intentionally uses pull requests for meaningful changes.

Before merging:

1. Check backup/snapshot status where applicable
2. Create or reference a change request
3. Document expected impact and rollback
4. Create a branch
5. Review the public diff for sensitive information
6. Open a pull request
7. Wait for repository checks
8. Merge only when the change is understood
9. Delete the branch after merge

See [docs/CHANGE-WORKFLOW.md](docs/CHANGE-WORKFLOW.md).

## Current Status

Active public documentation baseline for a security-focused homelab.

## Getting Started

1. [Homelab overview](docs/00-overview.md)
2. [Network documentation](docs/01-network.md)
3. [Security checklist](docs/03-security.md)
4. [Backup and restore](docs/04-backups.md)
5. [Disaster recovery](docs/05-disaster-recovery.md)
6. [Change workflow](docs/CHANGE-WORKFLOW.md)

## Maintainer

Maintained by [@1n50mn14c933k](https://github.com/1n50mn14c933k).
