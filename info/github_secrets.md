
## How should I set up my Github Action?
## To securely store credentials and configuration values required for GitHub Actions, follow these steps:

[__Step 1__]:
- Ensure the Workflow is in the Main Branch

- Before setting up secrets, confirm that your workflow files are located in the main branch of your repository.

[__Step 2__]: 
- Navigate to GitHub Secrets

- Go to your repository on GitHub.

- Click on Settings.

- In the left sidebar, click Secrets and variables > Actions.

- Click New repository secret.

[__Step 3__]: 

- Add Required Secrets
  
- Create the following secrets one by one:

- Secret Name: DEV_THOUGHTSPOT_URL , Value: Your Dev Org URL

- Secret Name: DEV_THOUGHTSPOT_USERNAME , Value: Admin Username of the cluster

- Secret Name: DEV_THOUGHTSPOT_SECRET_KEY , Value: Admin Password

[__Step 4__]: 
- Verify and Use Secrets in Workflows

- After adding secrets, they can be accessed within GitHub Actions using ${{ secrets.SECRET_NAME }}.

- Ensure your workflows correctly reference these secrets for authentication and deployment.
