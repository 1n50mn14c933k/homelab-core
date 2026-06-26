# Change Workflow

This document describes the safe workflow for making changes in this homelab repository.

The goal is simple:

> No random changes directly to `main`.
> Every change should be planned, reviewed, checked, and recoverable.

## Golden Rule

Before making a change, ask:

1. Do I have a backup or snapshot?
2. Do I know what this change affects?
3. Can I roll it back?
4. Am I about to expose secrets?
5. Is this change documented?

If the answer is unclear, stop and document it first.

## Standard Workflow

Use this workflow for every meaningful change.

### 1. Open an Issue

Create an issue before changing files.

The issue should explain:

* What will change
* Why it is needed
* What systems or docs are affected
* Backup or snapshot status
* Rollback plan
* Security impact

### 2. Create a Branch

Use a clear branch name.

Examples:

```text
docs/update-network-overview
security/add-hardening-checklist
backup/document-restore-test
inventory/update-example-hosts
```

Do not work directly on `main`.

### 3. Make the Change

Edit only what is needed.

Before committing, check that you are not adding:

* Passwords
* API keys
* SSH private keys
* VPN private keys
* Real internal IP maps
* Firewall exports
* Backup credentials
* Serial numbers
* Real `.env` files

### 4. Open a Pull Request

Every change should go through a pull request.

The pull request should explain:

* What changed
* Why it changed
* What was tested
* Security impact
* Rollback steps

### 5. Wait for Checks

GitHub Actions should pass before merging.

If checks fail:

1. Read the error
2. Fix the branch
3. Push again
4. Wait for checks again

### 6. Merge

Merge only when:

* The change is understood
* The pull request description is complete
* No secrets were added
* Checks passed
* Rollback is documented if needed

### 7. Delete the Branch

After merging, delete the branch to keep the repository clean.

## Emergency Changes

Emergency changes are allowed only when something is broken and waiting would make things worse.

Even then:

1. Make the smallest possible change
2. Document what happened afterward
3. Create a follow-up issue
4. Add rollback notes
5. Review whether monitoring or backups need improvement

## Commit Message Examples

Good commit messages:

```text
docs: add backup restore checklist
security: document SSH hardening baseline
inventory: add sanitized host examples
ci: add repository hygiene workflow
```

Bad commit messages:

```text
update
fix
stuff
changes
final
```

## Before Every Merge Checklist

Use this checklist before merging:

* [ ] Backup or snapshot status checked
* [ ] No secrets committed
* [ ] No real private keys committed
* [ ] No real credentials committed
* [ ] Public/private information separated
* [ ] Impact documented
* [ ] Rollback documented
* [ ] GitHub Actions passed
* [ ] Pull request description completed
