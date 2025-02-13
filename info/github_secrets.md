
## How should I set up my Github Action?
## To securely store credentials and configuration values required for GitHub Actions, follow these steps:

> [!CAUTION]
> Ensure the Workflow is in the Main Branch

[__Step 1__]: 
- Navigate to GitHub Secrets

- Go to your repository on GitHub.

- Click on Settings.

- In the left sidebar, click Secrets and variables > Actions.

- Click New repository secret.

[__Step 2__]: 

- Add Required Secrets
  
- Create the following secrets one by one:

- Secret Name: DEV_THOUGHTSPOT_URL , Value: Your Dev Org URL

- Secret Name: DEV_THOUGHTSPOT_USERNAME , Value: Admin Username of the cluster

- Secret Name: DEV_THOUGHTSPOT_SECRET_KEY , Value: Trusted Auth

- Secret Name: DEV_THOUGHTSPOT_PASSWORD , Value: Admin Password

> [!NOTE]
> If you are using CI/CD for same cluster, you only need these 3 secrets but if there is another cluster please configure the secret for Prod also with PROD_ Suffix

[__Step 3__]: 
- Verify and Use Secrets in Workflows

- After adding secrets, they can be accessed within GitHub Actions using ${{ secrets.SECRET_NAME }}.

- Ensure your workflows correctly reference these secrets for authentication and deployment.
