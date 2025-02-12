### Pull Request Validation: Ensuring Compatibility Before Merging

To maintain consistency and avoid conflicts when merging changes, we enforce validation tests between environments. If these tests fail, **the pull request should not be merged**.

## Validation Types

### 1. **Validation Between GitHub Branches**

Before merging changes between branches, we must ensure compatibility between the environments. This prevents potential failures in downstream deployments.

- We achieve this using the [__validate_API__](https://developers.thoughtspot.com/docs/git-api#_validate_merge).
- Our workflow automates this validation through [__validate_git_merge__](.github/workflows/validate_git_merge.yml).
- If the validation fails, **the pull request should be blocked**.
- If conflicts are detected, resolve them with a new commit before attempting the merge again.

### 2. **Validation Between Organizations (Orgs)**

When modifying TML content, we must ensure that the destination environment can import the changes without issues.

- This prevents unintended modifications in the target environment after merging changes from the development branch.
- Our workflow runs validation using [__validate_ts_content__](.github/workflows/validate_ts_content.yml).
- If the validation fails, the pull request **must not be merged** until the conflicts are resolved.

### Enforcement

- **All PRs must pass these validation tests before merging.**
- If any test fails, the PR should remain open until the issues are fixed.
- This ensures smooth deployments and consistency across environments.
