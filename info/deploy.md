### Deployment Process: Moving Objects from Dev to Prod

## Once the object commited to ts-dev branch, then following steps ensure a smooth deployment:

- After an object moves to the ts-dev branch in GitHub, create a [__Pull Request__](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to move it to the ts-prod branch.

- Fill in the required details in the PR Template to get it reviewed by an admin.

- During the review process, a [__Validate Test__](info/validate.md) will run to ensure the TML content in the target environment can be imported without conflicts.

- If the validate test passes, the changes will be merged into the ts-prod branch.

- Merging triggers the [__Deploy Workflow__](.github/workflows/deploy.yml), which picks the latest object from the PR and imports it into the production environment.

- The deploy API is triggered automatically, ensuring that the deployment process is carried out seamlessly.

## This structured approach ensures a seamless and conflict-free deployment process.

