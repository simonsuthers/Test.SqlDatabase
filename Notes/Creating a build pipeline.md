# Creating a build pipeline

A build pipeline implements Continuous Integration. It can automate buildong of code and running tests when code is committed.

- [Creating a build pipeline](#Creating-a-build-pipeline)
- [Add jobs to the pipeline](#Add-jobs-to-the-pipeline)
- [Run the build pipeline](#Run-the-build-pipeline)
- [Implementing Continuous Integration](#Implementing-Continuous-Integration)

## Creating a build pipeline

Go to Pipelines, then click on create pipeline::

<img src="./Pictures/BuildPipeline/Build01.png" width="50%" height="50%">

Click on use the classic editor to use the GUI to create the pipeline:

<img src="./Pictures/BuildPipeline/Build02.png" width="50%" height="50%">

Select the current repo where the code is stored, then press continue:

<img src="./Pictures/BuildPipeline/Build03.png" width="50%" height="50%">

Choose an empty job as the template:

<img src="./Pictures/BuildPipeline/Build04.png" width="50%" height="50%">

## Add jobs to the pipeline
Jobs are actions executed by the pipeline. This example has 1 job that has 4 tasks:
- Build the solution
- Run tests in the solution
- Create an artifcact of the solution using the Copy Files task
- Publish the artifacts

An agent job is created automatically. Click on the + sign to add a task:

<img src="./Pictures/BuildPipeline/Build05.png" width="50%" height="50%">

Find the Visual Studio build task and add it:

<img src="./Pictures/BuildPipeline/Build06.png" width="50%" height="50%">

Set the relevant settings. In this example, only the database project is built:

<img src="./Pictures/BuildPipeline/Build07.png" width="50%" height="50%">

Click o the + sign again and find the Copy files task:

<img src="./Pictures/BuildPipeline/Build08.png" width="50%" height="50%">

Use the info buttons to add the relevatn defaults:
- Source folder:  $(agent.builddirectory)\s
- Target folder: $(build.artifactstagingdirectory)

<img src="./Pictures/BuildPipeline/Build09.png" width="50%" height="50%">

Click on the + sign and find Publish Build artifacts:

<img src="./Pictures/BuildPipeline/Build10.png" width="50%" height="50%">

Set the relevant settings, then click on save:
- Path to Puslish: $(Build.ArtifactStagingDirectory)

<img src="./Pictures/BuildPipeline/Build11.png" width="50%" height="50%">

## Run the build pipeline

In the main pipeline window, click on the pipeline:

<img src="./Pictures/BuildPipeline/Build12.png" width="50%" height="50%">

To run the pipeline, click on Run Pipeline:

<img src="./Pictures/BuildPipeline/Build13.png" width="50%" height="50%">

In the pop-up, press run:

<img src="./Pictures/BuildPipeline/Build14.png" width="20%" height="20%">

## Implementing Continuous Integration
