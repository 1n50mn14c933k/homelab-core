# Network Documentation

This file contains **sanitized network architecture guidance only**.

## Public Documentation Rules

Use documentation networks such as:

- `192.0.2.0/24`
- `198.51.100.0/24`
- `203.0.113.0/24`

Do not publish real internal IP maps, public management endpoints, VPN keys, firewall exports, router/controller backups, private DNS zones, ISP details, sensitive hostnames, or MAC-address inventories.

## Segmentation Principles

- Separate management traffic from user and untrusted networks
- Isolate guest/IoT/untrusted devices where practical
- Do not expose admin interfaces directly to the public internet
- Use authenticated least-privilege remote administration paths
- Document DNS/DHCP changes and rollback
- Document firewall impact and rollback

## Public Checklist

- [ ] Management access is separated
- [ ] Guest/untrusted devices are isolated
- [ ] Admin interfaces are not public
- [ ] DNS/DHCP changes are documented
- [ ] Firewall changes include rollback notes
- [ ] Public examples use documentation networks only
