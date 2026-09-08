# Security Checklist

## Repository Safety

- [ ] No real `.env` files
- [ ] No private keys
- [ ] No API tokens
- [ ] No recovery codes
- [ ] No certificates with private key material
- [ ] No real internal IP maps
- [ ] No sensitive hostnames/usernames
- [ ] No firewall/router/DNS exports
- [ ] No serial numbers or asset identifiers
- [ ] No customer/third-party data
- [ ] Screenshots/logs sanitized

## Identity and Access

- [ ] Least privilege applied
- [ ] MFA enabled where supported
- [ ] Shared administrator accounts avoided
- [ ] Service accounts scoped
- [ ] Stale accounts/credentials removed
- [ ] Remote administration restricted

## System Hardening

- [ ] Security updates reviewed
- [ ] Unnecessary services disabled
- [ ] Admin interfaces restricted
- [ ] Firewall policy defined
- [ ] Default credentials disabled/changed
- [ ] Secrets stored outside source control

## Detection and Resilience

- [ ] Logs collected
- [ ] Important services monitored
- [ ] Security events can alert
- [ ] Backups tested
- [ ] Recovery procedures documented

## Change Control

- [ ] Backup/snapshot checked
- [ ] Change request created
- [ ] Impact documented
- [ ] Rollback documented
- [ ] Public diff reviewed
- [ ] Repository checks pass
