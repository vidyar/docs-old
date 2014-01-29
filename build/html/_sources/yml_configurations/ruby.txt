:title: Ruby yml files
:description: configuring yml files for Ruby
:keywords: ruby,rvm,gemfile

.. _ruby_yml_file:

Yml file Ruby
===============
This section helps you to build environment and configuration topics specific to Ruby projects.
**Ruby versions for testing :**

We support for all the ruby versions, as it installs the project dependencies automatically.

Ruby workers uses RVM to provide various versions of ruby projects . To specify them, use rvm: key in your shippable.yml file, for example:

.. code-block:: bash 

	language: ruby
	rvm:
  	  - 2.0.0
      - 1.9.3
    script: rake test


**Test Scripts:**

We are using Bundler to install your project's dependencies and run rake by default to execute your tests.
Please note that you need to add rake to your Gemfile.
It is possible to override this behaviour and there are project that use RVM gemset import feature but the majority of Ruby projects hosted on Shippable uses Bundler.

You can specify a custom Gemfile name:

.. code-block:: bash
	
	gemfile: gemfiles/Gemfile.ci


Unless specified, the worker will look for a file named "Gemfile" in the root of your project.

You can also set extra arguments to be passed to bundle install:

.. code-block:: bash

	bundler_args: --binstubs 


You can also define a script to be run before 'bundle install':

.. code-block:: bash

	before_install: some_command 


Please refer the Ruby-buildsample example for more details.


