Memcached is an in-memory key-value store for small chunks of arbitrary data (strings, objects) from results of database calls, API calls, or page rendering.

Memcached is also not started on boot.Add the the following to your shippable.yml file to start the service for your project.
The default port value to connect on memcached service is 11211.

services:
  - memcached
You can also add the version numbers specific to your projects in the yml file. If you are not mentioning it, then by default your build will run against the latest version.

services:
  - memcached-2.2.3
You can also refer the example Memcache-buildsample on github for more details.
