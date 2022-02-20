# Creating a deployment group

Deployment groups create a tunnel between Azure Devops and a deployment machine

- [Create Github PAT](#Create-Github-PAT)
- [Import Repo to Azure](#Import-Repo-to-Azure)

## Creating a deployment group

Go Deployment Groups and click on create:

<img src="./Pictures/DeploymentGroups/DeploymentGroup01.png" width="50%" height="50%">

Enter a name, tick the Use Personal Access Token box, then copy the token to the clipboard:

<img src="./Pictures/DeploymentGroups/DeploymentGroup02.png" width="50%" height="50%">

Paste the token on the clipboard into PowerShell and run. PowerShell should be running as administator. Use the PowerShell command as the ISE does not work:

<img src="./Pictures/DeploymentGroups/DeploymentGroup03.png" width="50%" height="50%">

Follow the defaults in PowerShell:

<img src="./Pictures/DeploymentGroups/DeploymentGroup04.png" width="50%" height="50%">

The machine should now appear in Azure Devops:

<img src="./Pictures/DeploymentGroups/DeploymentGroup05.png" width="50%" height="50%">

## Adding a tag to the deployment group

<img src="./Pictures/DeploymentGroups/DeploymentGroup06.png" width="50%" height="50%">

## Setting the user for the deployment group

<img src="./Pictures/DeploymentGroups/DeploymentGroup07.png" width="50%" height="50%">

