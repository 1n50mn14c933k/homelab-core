# Server Documentation

This file documents sanitized server roles and baseline requirements.

## Server Role Template

| Field | Example |
| --- | --- |
| Hostname | `host01.example` |
| Role | Docker host, monitoring, backup, identity |
| OS | Debian, Ubuntu Server, Talos, Proxmox |
| Environment | Lab, test, staging |
| Backup required | Yes or no |
| Monitoring required | Yes or no |
| Exposure | Internal, VPN-only, reverse-proxied |

## Baseline Checklist

- [ ] Security updates reviewed and applied
- [ ] Remote administration hardened
- [ ] Default/unused accounts removed or disabled
- [ ] Firewall policy defined
- [ ] Least-privilege administration used
- [ ] MFA enabled where supported
- [ ] Monitoring/logging configured
- [ ] Backup/snapshot plan documented
- [ ] Restore procedure known
- [ ] Public documentation contains no real credentials or inventory values

Document the security pattern, not unnecessary identifying details.
