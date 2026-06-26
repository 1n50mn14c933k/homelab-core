# Scripts

Helper scripts may be documented here.

## Script Safety Rules

- Scripts must not contain real credentials
- Scripts must not print secrets into logs
- Scripts should use `.env.example` or documented variables
- Destructive scripts must include warnings and rollback notes
- Prefer dry-run modes where possible
