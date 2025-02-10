## Creating Config in TS
- Best Pratice to create config for version Control is to create it through [__V2 API__](https://developers.thoughtspot.com/docs/restV2-playground?apiResourceId=http%2Fapi-endpoints%2Fversion-control%2Fcreate-config)
- In config we got option like

  - repository_url -> https://github.com/thoughtspot/ts-ci-github
  - username -> user with admin priviledge
  - access_token -> Token provided by github so TS can access 
  - branch_names -> Ex. Branch name for which we are creating this Config 
  - enable_guid_mapping -> True by default
  - configuration_branch_name -> create a separate config branch with name ts-config

- TRY IT OUT and you will get success message
- You can check the Config the you created using the [__Search Config__](https://developers.thoughtspot.com/docs/restV2-playground?apiResourceId=http%2Fapi-endpoints%2Fversion-control%2Fsearch-config)
- Repeat the same steps for other Org
