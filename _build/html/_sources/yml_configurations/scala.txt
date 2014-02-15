:title: scala 
:description: configuring yml file for scala
:keywords: scala,SBT,OracleJDK6,OracleJDK7,OpenJDK6,OpenJDK7 

.. _scala:

scala 
======

This section helps you to build environment and configuration topics specific to Scala projects.

We support for SBT,oraclejdk6, oraclejdk7 ,openjdk6 and openjdk7 . Specify scala versions like 2.8.x, 2.9.x and 2.10.x in the shippable.yml file as shown below.


**Dependency Management :** Since Scala builder assumes dependency management based on the projeccts like maven ,gradle or SBT, it will pull down project dependencies automatically before running tests.

.. code-block:: bash 

	language: scala
	scala:
   	   - 2.8.2
   	   - 2.9.2


To test against multiple JDKs, use the jdk: .For example, to test against the Oracle JDK 7 and OpenJDK 6:

.. code-block:: bash

	jdk:
  	- oraclejdk7
  	- openjdk6

To test against OpenJDK 7 and Oracle JDK 7:

.. code-block:: bash

	jdk:
  	  - openjdk7
	  - oraclejdk7
    
**SBT projects :**

Test command: If your repository root contains project directory or build.sbt file ,then Scala builder will use sbt ++$SHIPPABLE_SCALA_VERSION test to run your test suite.

Please refer the :ref:`Scala_buildsample` example for more details.
