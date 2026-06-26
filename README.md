# homelab-core

Main documentation hub for my security-focused homelab.

This repository contains sanitized documentation, architecture notes, templates, and operating procedures for building and maintaining a repeatable homelab environment.

## Purpose

The goal of this repository is to document a homelab in a way that is:

* Secure by default
* Easy to rebuild
* Clear for future troubleshooting
* Safe to publish publicly
* Useful for learning real-world infrastructure practices

This repository does **not** contain real secrets, private keys, passwords, internal IP maps, firewall exports, or sensitive inventory.

## Homelab Focus

* Linux administration
* Server hardening
* Docker and Compose security
* Network monitoring
* Logging and alerting
* Backup and restore testing
* Ansible automation
* Disaster recovery planning
* Infrastructure documentation

## Security Principles

| Principle                    | How it is applied                                                 |
| ---------------------------- | ----------------------------------------------------------------- |
| No secrets in Git            | Secrets, keys, tokens, and credentials are never committed        |
| Least privilege              | Services, users, and tokens only get the access they need         |
| Repeatable builds            | Systems should be rebuildable from documentation and automation   |
| Backups before changes       | Snapshots or backups are checked before major changes             |
| Monitoring before production | Services should be observable before being trusted                |
| Public/private separation    | Sanitized examples stay public; sensitive inventory stays private |

## Repository Map

```text
homelab-core/
├── README.md
├── SECURITY.md
├── .github/
│   ├── CODEOWNERS
│   ├── dependabot.yml
│   └── workflows/
│       └── repository-hygiene.yml
├── docs/
│   ├── 00-overview.md
│   ├── 01-network.md
│   ├── 02-servers.md
│   ├── 03-security.md
│   ├── 04-backups.md
│   └── 05-disaster-recovery.md
├── inventory/
│   ├── hosts.example.yml
│   └── services.example.yml
├── diagrams/
│   └── README.md
└── scripts/
    └── README.md
```

## Documentation Sections

| Section                        | Purpose                                                 |
| ------------------------------ | ------------------------------------------------------- |
| `docs/00-overview.md`          | High-level lab goals, scope, and architecture           |
| `docs/01-network.md`           | Sanitized network design and segmentation notes         |
| `docs/02-servers.md`           | Server roles, operating systems, and baseline setup     |
| `docs/03-security.md`          | Hardening notes, access control, and security checklist |
| `docs/04-backups.md`           | Backup strategy, snapshot rules, and restore testing    |
| `docs/05-disaster-recovery.md` | Recovery procedures and rebuild planning                |
| `inventory/`                   | Example inventory files only                            |
| `diagrams/`                    | Sanitized diagrams and diagram notes                    |
| `scripts/`                     | Helper scripts and script documentation                 |

## What Belongs Here

This public repository may contain:

* Sanitized documentation
* Example configurations
* Example inventory files
* Architecture notes without sensitive values
* Security checklists
* Backup and recovery procedures
* Diagrams without real public/private addressing
* Automation examples without secrets

## What Does Not Belong Here

Do **not** commit:

* Real passwords
* API tokens
* SSH private keys
* VPN private keys
* Internal IP maps
* Firewall exports
* Router backups
* Backup repository credentials
* Serial numbers
* Customer or third-party data
* Real `.env` files

Use the private repository `private-lab-inventory` for sensitive lab notes and real inventory details.

## Change Workflow

Before making changes:

1. Check backup or snapshot status
2. Create an issue describing the change
3. Document the expected impact
4. Create a branch
5. Open a pull request
6. Wait for checks to pass
7. Merge only after review or owner approval
8. Document rollback steps when needed

## Current Status

This repository is in the initial foundation stage.

Current focus:

* Repository security baseline
* README and documentation structure
* CODEOWNERS
* Dependabot configuration
* GitHub Actions hygiene checks
* Security policy
* Sanitized starter documentation

## Getting Started

Start reading here:

1. `docs/00-overview.md`
2. `docs/01-network.md`
3. `docs/03-security.md`
4. `docs/04-backups.md`
5. `docs/05-disaster-recovery.md`

If you are copying this structure for your own lab, replace all example names, networks, and services with sanitized values before publishing.

## Maintainer

Maintained by [@1n50mn14c933k](https://github.com/1n50mn14c933k).

This project is part of a security-focused homelab documentation and learning environment.
