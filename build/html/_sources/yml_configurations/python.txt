:title: Python yml file
:description: Configuring yml file for python
:keywords: Python, pip, nosetests, mirrors

.. _python_yml_file:

Python Yml file
===============

This section helps you to build environment and configuration topics specific to Python projects.

**Choosing Python versions to test against :**

We support for the following python versions

*   2.6
*   2.7
*   3.0
*   3.1
*   3.2
*   3.3

To provide several Python versions your projects can be tested against, use python: key in your shippable.yml file, for example:

.. code-block:: bash

	language: python
	python:
  	  - "2.6"
          - "2.7"
          - "3.2"
          - "3.3"
	# command to install dependencies
	install: "pip install -r requirements.txt --use-mirrors"
	# command to run tests
	script: nosetests


**Test Scripts :**

Python projects need to provide script key in their shippable.yml to specify what command to run tests with.
For example, if your project is tested by running nosetests, specify it like this:

.. code-block:: bash

	# command to run tests
	script: nosetests


In case script key is not provided in shippable.yml for Python projects, Python builder will print a message and fail the build.

**Our CI uses pip:**

By default our CI uses pip to manage your project's dependencies.

The command is

.. code-block:: bash
	
	pip install -r requirements.txt --use-mirrors


We highly recommend using --use-mirrors if you override dependency installation command to reduce the load on PyPI and possibility of installation failures.

**Pre-installed packages:**

Few packages are pre-installed in each virtualenv by default to ease running tests:

   * pytest
   * nose
   * mock

Please refer the Python -buildsample example for more details.
