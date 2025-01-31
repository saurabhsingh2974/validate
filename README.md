
# ThoughtSpot CI

Manage your ThoughtSpot objects with the [__Verion Control APIs__](https://developers.thoughtspot.com/docs/rest-apiv2-reference#_version_control) and [__Github Actions__](https://github.com/features/actions).

## Quickstart

  1. __[Fork this repo](https://github.com/thoughtspot/ts-ci-github/fork)__.
  2. [__Configure your Org(s)__](info/config.md).
  3. [__Configure your GitHub Secrets__](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository) to manage authenticatation to __ThoughtSpot__.
  4. Customize the [__workflow files__](.github/workflows/) to your needs.

## What secrets do I need to manage in GitHub?

__ThoughtSpot__ [__requires an authenticated session__](https://developers.thoughtspot.com/docs/api-authv2) in order to use the APIs. Each of the workflows will ask for 3 secrets.

  - `THOUGHTSPOT_URL` - your ThoughtSpot URL (eg. __https://company.thoughtspot.cloud__)
  - `THOUGHTSPOT_USERNAME` - an Administrator-level user

  As well as either one of ..

  - `THOUGHTSPOT_SECRET_KEY` - your cluster-level __ThoughtSpot__ [__secret key__](https://developers.thoughtspot.com/docs/trusted-auth-secret-key)
  - `THOUGHTSPOT_PASSWORD` - your user's __ThoughtSpot__ __password__

## How to Use / Guides

  1. [__How do I fetch changes from ThoughtSpot?__](info/commit.md)
  2. [__How do I check my changes before pushing to a new environment?__](info/validate.md)
  3. [__How do I deploy changes to a new ThoughtSpot environment?__](info/deploy.md)

## Want to contribute?

See our [__contributing guide__](CONTRIBUTING.md) :heart: