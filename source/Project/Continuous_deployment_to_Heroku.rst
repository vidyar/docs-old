:title: Continuous deployment to Heroku
:description: deployment configurations to heroku in shippable.yml file
:keywords: Heroku, SSH key, deployment
 
.. _Continuous_deployment_to_Heroku:

Continuous deployment to Heroku:
================================

Heroku supports Ruby, Node.js, Python, so you can use these languages to build and deploy apps on Heroku. You can deploy to your own server by adding the custom after_success: .

For this you need to add the Public key that was generated for your subscription in shippable to set up continous deployment on providers.

* Go to settings and copy the SSH Key or public key generated for your subscription.

* Log In to Heroku and add the SSH key to your account 


.. image:: images/Heroku-ssh.png


A Sample deployment configurations to your shippable.yml file is given below .

.. code_block:: bash

	after_success :
	git push deploy Git URL


You need to copy the Git URL from your project for deployment in heroku .


* Go to apps and select your project.

* Go to the settings page of your project and copy the Git URL. 


.. image:: images/Heroku-url.png


* Add it to the shippable.yml file. 

An example is given below :

.. code_block:: bash

	after_success :
	git push deploy git@heroku.com:shroudd-headland-1758.git

