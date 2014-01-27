Redis is an open source, BSD licensed, advanced key-value store. It is often referred to as a data structure server since keys can contain strings, hashes, lists, sets and sorted sets.
Redis is also not started on boot. Add the service to the shippable.yml file to start service for your project. 
The default port value to connect on redis service is 6379.

services:
  - redis
You can also add the version numbers specific to your projects as shown below. If you are not mentioning it, then by default your build will run against the latest version.

services:
  - redis-2.6.16
You can also refer the example Redis-buildsample on github for more details.
