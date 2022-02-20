# Import Repo to Azure Devops

- [Create Github PAT](#Create-Github-PAT)
- [Import Repo to Azure](#Import-Repo-to-Azure)

## Create Github PAT
Go to github settings

<img src="./Pictures/01GithubSettings.png" width="50%" height="50%">

In settings, find developer settings:

<img src="./Pictures/02GithubDeveloperSettings.png" width="50%" height="50%">

Click on Personal Access Tokens, then click on Generate new token:

<img src="./Pictures/03GithubCreatePAT.png" width="50%" height="50%">

Enter a name for the token, then copy the token to the clipboard:

<img src="./Pictures/05GithubTokenScope.png" width="50%" height="50%">

## Import Repo to Azure
In Azure Devops, go to Repos:

<img src="./Pictures/ImportRepo01.png" width="25%" height="25%">

In the Repo, find Import Repository:

<img src="./Pictures/ImportRepo02.png" width="50%" height="50%">

Enter the url, PAT token and user name (the user name is the account name, not the login details from GitHub):

<img src="./Pictures/ImportRepo03.png" width="25%" height="25%">


