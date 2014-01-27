:title: Elastic search
:description: adding elastic search service to shippable.yml
:keywords: Elastic search, service, version numbers

.. _Elastic_search:

Elastic search:
================
 
Elasticsearch is a powerful open source search and analytics engine that makes data easy to explore.Since Elastic search is not started on boot , you need to add elasticsearch to the shippable.yml file to start the service for your project.

The default port value to connect on elastic search service is 9200.

.. code_block:: bash
	services:
  	  - elasticsearch

You can also add the version numbers specific to your projects in the yml file. If you are not mentioning it, then by default your build will run against the latest version.

.. code_block:: bash
	services:
  	  - elasticsearch-0.20.5

You can also refer the example Elasticsearch-buildsample on github for more details.


