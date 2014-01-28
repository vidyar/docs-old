:title: configuring yml files
:description:  how to write yml file
:keywords: yml file, csharp, nodejs, python, java,scala,ruby, link

Configuring yml file
========================


Our CI environment needs a little information about your project to pick up the type of builds to be executed.The information might be the programming language ,build environment ,version number and the notification alert type.
Make a note of all these information in a notepad and save it as "shippable.yml" and add it to the root of your repository.

Build_environment is the environment needed to run your build.It can be Windows 2012 or Ubuntu 12.04 LTS.Write it as win2012 for windows project and ubuntu1204 for ubuntu project.

Before_install script will make sure the required dependencies are installed.

Language is used to specify the programming language that you have used in your program.

Notification alerts :Get Notification alerts to the mentioned recipients id in the shippable .yml file.

A basic shippable.yml file is -

.. code-block:: bash

	language: ruby
	rvm:
    	  - "1.9.2"
          - "1.9.3"
	notifications:
  	   email:
    		exampleone@org.com
    		exampletwo@org.com

    

This will just run the jobs using ruby 1.9.2 and 1.9.3 and creates separate build for each version.It sends an email notification to the mentioned mail recipients for both builds.

We will support for .travis.yml ,if you have already one, then you should be good to go with that!

Please note that the yml file is case-sensitive.You should be very carefull while writing yml file.

The following procedure guides you to build and test your projects using Shippable CI.

Currently we support the following languages.

1.csharp

2.Java

3.Node.js

4.Python

5.Ruby

6.Scala


.. toctree::
   :maxdepth: 1
    
    yml
    Csharp
    Java
    Node.js
    Python
    Ruby
    Scala



