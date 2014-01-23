:title: configuring java yml file
:description: How to configure shippable.yml file for java 
:keywords: yml,java,maven,oraclejdk6,openjdk6,oraclejdk7,openjdk7

Java: 
==============================
This section helps you to create a shippable.yml file for your Java project.

We support for Ant, Maven, Gradle 1.4, OpenJDK 6, OpenJDK 7 and Oracle JDK 7. A sample shippable .yml file for Java is given below for multiple JDK's test:

.. code-block:: bash
	language: java
 	jdk:
   	   - oraclejdk7
   	   - openjdk6
And testing with Open JDK 7 and Oracle JDK 7 

.. code-block:: bash
	jdk:
  	  - openjdk7
  	  - oraclejdk7

**Maven projects**
Test command : If your project has pom.xml file in the repository root ,then Our Java builder will use Maven 3 to build it. By default it will use mvn test to run the test suite.

Dependency Management : Before running tests, Java builder will execute the below line to install your project's dependencies with Maven.



**Maven projects**
Test command : If your project has pom.xml file in the repository root ,then Our Java builder will use Maven 3 to build it. By default it will use mvn test to run the test suite.

Dependency Management : Before running tests, Java builder will execute the below line to install your project's dependencies with Maven.


**Maven projects**
Test command : If your project has pom.xml file in the repository root ,then Our Java builder will use Maven 3 to build it. By default it will use mvn test to run the test suite.

Dependency Management : Before running tests, Java builder will execute the below line to install your project's dependencies with Maven.

.. code-block:: bash
	mvn install -DskipTests=true

**Gradle projects**

Test command :If your project has "build.gradle" file in the repository root ,then Our Java builder will use Gradle to build it. By default it will use gradle check to run the test suite.

Dependency Management: Before running tests, Java builder will execute the below line to install your project's dependencies with Gradle.
.. code-block:: bash
        gradle assemble

**Ant Projects**

Test command :If your file does not contain gradle or maven files ,then Our Java builder will use Ant to build it. By default it will use Ant test to run the test suite.

Dependency Management: Since there are no standard way to install, You need to specify the install: key to install your project dependencies with Ant.

.. code-block:: bash
	language: java
	install: ant deps

Please refer the Java-buildsample example for more details.
