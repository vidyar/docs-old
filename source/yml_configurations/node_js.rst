:title: Node_js yml file
:description: configuring yml file for node_js
:keywords: node_js, mocha, npm, node

.. _nodejs_yml file:

Node.js yml file
===============

This section helps you to build environment and configuration topics specific to Node.js projects. 

**Choosing Node versions to test against :**

We recommend that you use multiple versions to test your Node.js project. Add the following to shippable.yml:

.. code-block:: json
	 
	language: node_js
	node_js:
  	  - "0.10"
          - "0.8"
          - "0.6"
        before_script: "npm install mocha"


This will help us to run your tests against the latest branch releases.

We support for all the Node.js Versions , as it installs the project dependencies automatically.


Test Script :

For projects using NPM, add the following

.. code-block:: bash
	
	npm test


To run your test suite.

Run your test suite using Vows:

You can tell npm how to run your test suite by adding a line in package.json. For example, to test using Vows:

.. code-block:: bash

	"scripts": {
        "test": "vows --spec"
	}


Run your test suite using Expresso :

To test using Expresso:

.. code-block:: bash

	"scripts": {
	"test": "expresso test/\*"
	}

Using NPM :

We are using NPM to install your project's dependencies.
It is possible to override this behavior and there are project that use different tooling but the majority of Node.js projects hosted on Shippable uses NPM, which is also bundled with Node starting with 0.6.0 release.

By default, Our CI will run

.. code-block:: bash

	npm install



Specify the version numbers and frameworks that you have used to build and run your project in the shippable.yml file.

Keep the test outputs in shippable/testresults and codecoverage output in shippable/codecoverage folder to get the reports parsed.Otherwise you will not find the reports in our CI.

Please refer the Node.js-buildsample example for more details.

