### Creating a Configuration in ThoughtSpot
## To ensure best practices in version control, it is recommended to create the configuration using the V2 API.

- Configuration Parameters
- When setting up the configuration, the following parameters must be defined:

  - repository_url → The URL of the GitHub repository (e.g., https://github.com/thoughtspot/ts-ci-github).
  - username → The username of an account with admin privileges.
  - access_token → A GitHub-provided token that allows ThoughtSpot to access the repository.
  - branch_names → The branch for which the configuration is being created.
  - enable_guid_mapping → Set to true by default.
  - configuration_branch_name → A separate configuration branch (recommended name: ts-config).

## Steps to Create the Configuration
- Use the V2 API to send a request with the above parameters.
- Upon successful execution, a success message will be displayed.
- Verify the newly created configuration using the [Search Config API].
- Repeat the process for any additional organizations that require configuration.

## By following these steps, you ensure a standardized and structured approach to version control configuration in ThoughtSpot.
