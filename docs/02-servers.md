# Server Documentation

This file documents sanitized server roles and baseline setup.

## Server Role Template

| Field | Example |
|---|---|
| Hostname | `host01.example` |
| Role | Docker host, monitoring, backup, identity |
| OS | Debian, Ubuntu Server, Talos, Proxmox |
| Environment | Lab, test, staging |
| Backup required | Yes or no |
| Monitoring required | Yes or no |

## Baseline Checklist

- [ ] Automatic security updates reviewed
- [ ] SSH hardened
- [ ] Firewall enabled
- [ ] Least-privilege user accounts configured
- [ ] Monitoring agent installed where needed
- [ ] Backup or snapshot plan documented
