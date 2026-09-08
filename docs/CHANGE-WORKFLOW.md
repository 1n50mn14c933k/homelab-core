# Change Workflow

This repository intentionally protects `main` and uses pull requests for meaningful changes.

## Golden Rule

Before changing anything, ask:

1. Do I have a backup or snapshot where applicable?
2. Do I understand the impact?
3. Can I roll it back?
4. Could this expose sensitive information?
5. Is the change documented clearly enough for future recovery?

## Standard Workflow

1. Open or reference a change request.
2. Create a descriptive branch.
3. Make the smallest necessary change.
4. Review the diff locally for correctness and public-safety exposure.
5. Open a pull request.
6. Wait for repository checks.
7. Merge only when the change, impact, and rollback are understood.
8. Delete the merged branch.

Before committing, verify you are not adding passwords, API keys, PATs, private keys, recovery codes, real internal IP maps, sensitive hostnames, firewall/router/DNS exports, backup credentials, serial numbers, real `.env` files, or sensitive screenshots/logs.

## Emergency Changes

Emergency infrastructure changes may happen outside GitHub when availability or security requires immediate action. After stabilization, document the event, final state, rollback/recovery notes, and publish only sanitized information.

## Commit Message Examples

```text
docs: add backup restore checklist
security: document SSH hardening baseline
inventory: add sanitized host examples
ci: strengthen repository hygiene workflow
```

## Before Every Merge

- [ ] Backup/snapshot status checked where applicable
- [ ] No secrets or credentials committed
- [ ] Public/private information separated
- [ ] Impact documented
- [ ] Rollback documented
- [ ] Public diff reviewed
- [ ] GitHub Actions passed
