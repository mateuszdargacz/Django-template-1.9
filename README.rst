pix
==============================

business contacts matching

.. image:: https://travis-ci.org/mateuszdargacz/Django-template-1.9.png
     :target: https://travis-ci.org/mateuszdargacz/Django-template-1.9/
     :alt: Build Status






Settings
------------

Moved to settings_.

.. _settings: http://cookiecutter-django.readthedocs.io/en/latest/settings.html

Basic Commands
--------------

Setting Up Your Users
^^^^^^^^^^^^^^^^^^^^^

* To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your console to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

* To create an **superuser account**, use this command::

    $ python manage.py createsuperuser

For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.

Test coverage
^^^^^^^^^^^^^

To run the tests, check your test coverage, and generate an HTML coverage report::

    $ coverage run manage.py test
    $ coverage html
    $ open htmlcov/index.html

Running tests with py.test
~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

  $ py.test

Live reloading and Sass CSS compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Moved to `Live reloading and SASS compilation`_.

.. _`Live reloading and SASS compilation`: http://cookiecutter-django.readthedocs.io/en/latest/live-reloading-and-sass-compilation.html



Celery
^^^^^^

This app comes with Celery.

To run a celery worker:

.. code-block:: bash

    cd pix
    celery -A pix.taskapp worker -l info

Please note: For Celery's import magic to work, it is important *where* the celery commands are run. If you are in the same folder with *manage.py*, you should be right.








Deployment
----------





Docker
^^^^^^
Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~
- docker
- docker-machine
- docker-compose

Running Project
~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

  docker-machine create --driver virtualbox pix
  docker-machine start pix
  eval "$(docker-machine env pix)"
  docker-compose build
  docker-compose up

Utilities
~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

  docker-machine ssh pix              # enter virtual machine environment
  docker exec -it container_name bash # enter container environment
  docker-machine ip pix               # show virtualmachine ip address


See detailed `cookiecutter-django Docker documentation`_.

.. _`cookiecutter-django Docker documentation`: http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html


