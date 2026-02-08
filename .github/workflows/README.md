# GitHub Actions Disabled

GitHub Actions are **explicitly disabled** for this repository.

## Why?

This repository is a fork and the owner has chosen to disable GitHub Actions to avoid:
- Unnecessary workflow runs when syncing with upstream
- Confusion about CI/CD pipeline ownership
- Resource usage on forked repository workflows

## How is this enforced?

1. All workflow files have been removed
2. A `disabled.yml` placeholder workflow exists that:
   - Has no trigger events (cannot run)
   - Contains a fail-safe `if: false` condition
   - Serves as a marker that Actions are intentionally disabled

## Need to enable GitHub Actions?

If you need to enable GitHub Actions for this repository:

1. Delete the `disabled.yml` file
2. Add your desired workflow files to this directory
3. Update or remove this README

## Syncing with upstream

When syncing with the upstream fork, new workflow files may be pulled. You should:
1. Review any new workflow files carefully
2. Decide whether to keep them or maintain the disabled state
3. If maintaining disabled state, delete the new workflows and keep `disabled.yml`
