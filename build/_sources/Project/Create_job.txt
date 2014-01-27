:title: creating a job
:description: steps followed to create a job
:keywords: Node selection, manage node, create a job, GitHub 

.. _creating_a_job:

Creating a job
===============

A Job is used to handle your build projects in our CI. You need to create a job for each repo you want to build.

**Node Selection**

Node is container that will run your builds and tests. So add the relevant node or build environment before running the builds. Select the build environment to run your job from the dashboard on the right side of window, if you have not selected it yet by clicking on the + button .


Node selection 

You can also delete or reset the node by clicking on the Manage node button. But remember that Deleting a node will result in all data being purged in relation to that node .

Follow the steps below for creating a job.

* Click on the Create a new job button in the left sidebar .

Createjob button 

* You can see a list of your repositories on the new modal window.Pick the relevant repository. 

Create a job 

* Shippable will automatically detect the list of branches available for your repository and the yml file to configure the job.

* A modal dialog will pop up,where you can select the Branch that you would like to build and test from the dropdown menu. 

Create a branch 

* If that branch has yml file, then we can use to configure the job. You just need to click on the Let's do this! button.

* You will get a Success message stating that "Your Job has been set up" and the job is updated in the jobs list menu in the left pane .
* You can create additional jobs if required by clicking on the Create a new job button .

To delete a job , just click the button next to the run button. It will ask you for confirmation. Click Yes. Your job will no longer exists in the Job pane.


