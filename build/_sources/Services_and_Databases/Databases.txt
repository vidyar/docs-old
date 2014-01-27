:title: Databases
:description:  configuring databases in shippable.yml file
:keywords: MongoDB, Mysql,Postgresql,sqlite3

.. _Databases :

Databases:
==========

MongoDB
-------

MongoDB is an open-source, document-oriented database designed for ease of development and scaling.
MongoDB will not start on boot. Add the service to the shippable.yml file to start service for your project and it binds to 127.0.0.1.

.. code_block:: bash
	
	services:
 	 - mongodb

You can also refer the example mongodb-buildsample on github for more details.


MySQL
-------

MySQL is started on boot, binds to 127.0.0.1 and requires authentication. You can connect to the databases using the username "shippable" and password is not required.

Create the myapp_test database first and run it as part of your build script.

.. code_block:: bash
	
	before_script:
  	  - mysql -e 'create database myapp_test;'
                                 

You can also refer the example mysql-buildsample on github for more details.


PostgreSQL
--------------

PostgreSQL is started on boot binds to 127.0.0.1 and requires authentication. You can connect to the databases using the username "postgres" and password is not required .

Create the database as part of your build process:

.. code_block:: bash

	before_script:
	  - psql -c 'create database myapp_test;' -U postgres


You can also refer the example postgresql-buildsample on github for more details.

SQLite3
------------

SQLite is a software library that implements a self-contained, serverless, zero-configuration, transactional SQL database engine. So you can use SQLite, if you do not want to test your code behaviour with other databases.

A sample project has been created using python. You can refer the example sqlite-buildsample on github for more details.


