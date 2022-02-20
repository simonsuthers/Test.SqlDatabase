# Creating a release pipeline

A release pipeline implements Continuous Delivery/Deployment. It can automatically deploy code to a database when it is checked in, as long as it meets the criteria set out in Continuous Integration.

- [Creating a release pipeline](#Creating-a-release-pipeline)
  - [#Add the Continuous Integration Artifact]#(Add-the-Continuous-Integration-Artifact) 
  - [#Add deployment target]#(Add-deployment-target) 
- [Enable Continuous Deployment](#Enable-Continuous-Deployment)
- [Run the build pipeline](#Run-the-build-pipeline)
- [Implementing Continuous Integration](#Implementing-Continuous-Integration)

## Creating a release pipeline
### Add the Continuous Integration Artifact

Go to Releases, then click on New pipeline::

<img src="./Pictures/ReleasePipeline/Release01.png" width="50%" height="50%">

Select **Empty job** as a template:

<img src="./Pictures/ReleasePipeline/Release02.png" width="50%" height="50%">

In the basic template, click on Add an artifact:

<img src="./Pictures/ReleasePipeline/Release03.png" width="50%" height="50%">

When adding the artifact, choose Build as source type and choose the build pipeline created earlier:

<img src="./Pictures/ReleasePipeline/Release04.png" width="50%" height="50%">

### Add deployment target

To add a deployment target, click the **n job n task** link in the stage:

<img src="./Pictures/ReleasePipeline/Release07.png" width="50%" height="50%">

Click on the ... for the stage and choose **Add a deployment group job**:

<img src="./Pictures/ReleasePipeline/Release10.png" width="50%" height="50%">

Give the deployemnt job a sensible name. Set the Deployment group setting o the deployment group created earlier and the Required Tag setting to the tag of the deployment group created earlier:
- Deployment group: SQL Server localhost
- Required tags: localhost database

<img src="./Pictures/ReleasePipeline/Release11.png" width="50%" height="50%">

For the agent job, click on the job and then press remove in the far right-hand side:

<img src="./Pictures/ReleasePipeline/Release12.png" width="50%" height="50%">

For the Deployment group job, click on the + sign to add a task:

<img src="./Pictures/ReleasePipeline/Release13.png" width="50%" height="50%">

Find the SQL Server database deploy task, and press add:

<img src="./Pictures/ReleasePipeline/Release14.png" width="50%" height="50%">

Set the dacpac file location to the location in the artifact. Also set the server name and database name:

<img src="./Pictures/ReleasePipeline/Release15.png" width="50%" height="50%">

## Enable Continuous Deployment

<img src="./Pictures/ReleasePipeline/Release05.png" width="50%" height="50%">

<img src="./Pictures/ReleasePipeline/Release06.png" width="50%" height="50%">
