:title: Services
:description: A brief description about the services supported in shippable
:keywords: Elastic Search, Memcached, Redis

.. _Services:

Services:
==========


Elastic Search
----------------


Elasticsearch is a powerful open source search and analytics engine that makes data easy to explore.Since Elastic search is not started on boot , you need to add elasticsearch to the shippable.yml file to start the service for your project.

The default port value to connect on elastic search service is 9200.

.. code-block:: bash

	services:
  	  - elasticsearch


You can also add the version numbers specific to your projects in the yml file. If you are not mentioning it, then by default your build will run against the latest version.

.. code-block:: bash

	services:
  	  - elasticsearch-0.20.5


You can also refer the example Elasticsearch-buildsample on github for more details.

Memcached
----------

Memcached is an in-memory key-value store for small chunks of arbitrary data (strings, objects) from results of database calls, API calls, or page rendering.

Memcached is also not started on boot.Add the the following to your shippable.yml file to start the service for your project.

The default port value to connect on memcached service is 11211.

.. code-block:: bash

	services:
  	  - memcached


You can also add the version numbers specific to your projects in the yml file. If you are not mentioning it, then by default your build will run against the latest version.

.. code-block:: bash

	services:
  	  - memcached-2.2.3

You can also refer the example Memcache-buildsample on github for more details.


Redis
---------


Redis is an open source, BSD licensed, advanced key-value store. It is often referred to as a data structure server since keys can contain strings, hashes, lists, sets and sorted sets.
Redis is also not started on boot. Add the service to the shippable.yml file to start service for your project.
The default port value to connect on redis service is 6379.

.. code-block:: bash

	services:
  	  - redis

You can also add the version numbers specific to your projects as shown below. If you are not mentioning it, then by default your build will run against the latest version.

.. code-block:: bash

	services:
  	  - redis-2.6.16


You can also refer the example Redis-buildsample on github for more details.
