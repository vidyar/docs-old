:title: Python-buildsample
:description: A brief description about Python-buildsample
:keywords: Python, Language,version number, Install, Notification alerts

.. _Python_buildsample :

Python-buildsample
==================== 

A sample repository `Python-buildsample <https://github.com/Shippable/Python-buildsample>`_ has been created using `nose <https://pypi.python.org/pypi/nose>`_ and `coverage 3.7  <https://pypi.python.org/pypi/coverage/>`_  .
Keep the test and code coverage outputs in our special folders called Shippable/testresults and Shippable/codecoverage to get the reports parsed and also the test results must be inJunit format.

We need the yml file to analyze the project details . So add the shippable.yml file to the root of your repo by specifying :


**Language :** python is used.

**version number :** Specify the version numbers against which your build needs to run. We are using "2.7".

**Install :** Install the required dependencies for your repo here.

**script :** Specify the command to run the test and coverage and save the results in their respective 
shippable folders. If you have not created the folders, then you can create it using the before_script key.

**Notification alerts:**  Email notifications are added to get the alerts about the build status.
Create a job by selecting the repo Python-buildsample and run it using Ubuntu 12.04LTS node. Once the build finishes execution, you can check for the console output, test and codecoverage results as well as the build trend graphs.
