# How Deploy Object From Dev To Prod
- After Object moves to ts-dev Branch in Github, we can raise [__Pull_Request__](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests#about-pull-requests) to move object to ts-prod Branch.
- Fill the PR Template (.github/pull_request_template.md) with necassary information to get it review by admin.
- During the Review a [__Validate__](.github/workflows/validate.yml) Test will run to check if we can to ensure the TML content in target environments can import changes without conflicts.
- After Successfull Test, we will merge oue changes to ts-prod branch, it will run [__Deploy_Workflow__](.github/workflows/deploy.yml) which will pick the recent object from PR, import these object production environment.

