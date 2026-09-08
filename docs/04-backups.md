# Backup and Restore

A backup is not trustworthy simply because a job reports success.

Backups should be **documented, monitored, tested, and restorable**.

## Backup Checklist

- [ ] Important data identified
- [ ] Backup scope documented
- [ ] Backup target documented privately
- [ ] Schedule defined
- [ ] Retention defined
- [ ] Failures generate visibility/alerts
- [ ] Restore test performed
- [ ] Recovery time expectations documented
- [ ] Credentials stored outside the repository
- [ ] Backup infrastructure protected
- [ ] At least one recovery path survives loss of the primary system

## Restore Test Template

| Date | System | Backup Source | Restore Target | Result | Notes |
| --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD | example-service | example-backup | isolated test system | Pass/Fail | Sanitized notes |

Do not publish real backup addresses, credentials, encryption keys, storage inventory, or off-site account details.
