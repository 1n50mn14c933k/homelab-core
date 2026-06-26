# Security Checklist

## Repository Safety

- [ ] No real `.env` files committed
- [ ] No private keys committed
- [ ] No API tokens committed
- [ ] No internal IP maps committed
- [ ] No customer or third-party data committed

## System Hardening

- [ ] Least privilege is applied
- [ ] MFA is enabled where supported
- [ ] Admin interfaces are restricted
- [ ] Logs are collected before production use
- [ ] Backups are tested, not only configured

## Change Control

- [ ] Backup or snapshot checked before change
- [ ] Issue created for meaningful change
- [ ] Expected impact documented
- [ ] Rollback documented
- [ ] Result documented after change
