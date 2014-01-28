:title: Csharp yml configuration
:description: yml file and versions supported
:keywords: yml, Csharp

.. _Csharp_yml:

Csharp:
--------
This section helps you to create a shippable.yml file for your csharp project.The information that we required are the version number , build environment , frameworks and the notification alert type.


Choosing .Net versions/implementations to test against:

We support for the following .Net versions

- 2.0 .
- 3.5 .
- 4.0 .
- 4.5 .

Build frameworks for .Net :

The frameworks that we support for .Net are

*  Msbuild
*  Nant 

sample shippable.yml file for csharp is given below :

.. code-block:: bash 
 
	language: csharp
 	csharp:
    	    " - dotNet40"
 	build_environment: win2012
 	before_install: msbuild Shouldly.sln


Specify the version numbers and frameworks that you have used to build and run your project in the shippable.yml file.

Keep the test outputs in shippable/testresults and output of codecoverage in shippable/codecoverage folder to get the reports parsed.Otherwise you will not find the reports in our CI.

Please refer the csharp-buildsample example for more details.
