# Network Documentation

This file contains sanitized network notes only.

## Public Documentation Rules

Use example networks only, such as:

- `192.0.2.0/24`
- `198.51.100.0/24`
- `203.0.113.0/24`

Do not publish real internal IP maps, VPN keys, firewall exports, router backups, ISP details, or externally reachable admin endpoints.

## Segmentation Checklist

- [ ] Management access is separated from user services
- [ ] Guest or untrusted devices are isolated
- [ ] Admin interfaces are not exposed publicly
- [ ] DNS and DHCP changes are documented
- [ ] Firewall changes include rollback notes
