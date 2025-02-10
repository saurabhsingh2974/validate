### Validating the objects between two environment
## There are two types of validation we can do 

1. **Between the Github Branches**

- Before moving the objects between two branches we should test the compability between these two environment
- for that we will use [__validate_API__](https://developers.thoughtspot.com/docs/git-api#_validate_merge).
- In our workflow we can validate between two branches through [__validate_git_merge__](.github/workflows/validate_git_merge.yml).
- After validating the merge, check for conflicts. Resolve issues if any with a new commit and merge your changes to the ts-prod branch.

2. **Between the Orgs**
- We can runs validation to detect if your destination environment can import the changes without conflicts.
- Use this when the TML content is modified between source and destination environments and if you do not want the TML content in your destination branch to be modified after a pull request from your dev branch.
- In our workflow we can validate between two branches through [__validate_ts_content__](.github/workflows/validate_ts_content.yml).
