immobiliare/sentry-php
======================

.. image:: https://secure.travis-ci.org/getsentry/sentry-php.png?branch=master
   :target: http://travis-ci.org/getsentry/sentry-php


This project is a fork of official PHP SDK v1.7.0 for `Sentry <https://getsentry.com/>`_ to work even with php5.2.

.. code-block:: php

    // Instantiate a new client with a compatible DSN and install built-in
    // handlers
    $sentryClient = new Raven_Client('https://e9ebbd88548a441288393c457ec90441:399aaee02d454e2ca91351f29bdc3a07@app.getsentry.com/3235');
    $sentryClient->install();

    // Capture an exception
    $event_id = $sentryClient->captureException($ex);

    // Give the user feedback
    echo "Sorry, there was an error!";
    echo "Your reference ID is " . $event_id;

For more information, see the `documentation <https://docs.getsentry.com/hosted/clients/php/>`_.


Contributing
------------

Dependencies are managed through composer:

::

    $ composer install


Tests can then be run via phpunit:

::

    $ vendor/bin/phpunit


Resources
---------

* `Documentation <https://docs.getsentry.com/hosted/clients/php/>`_
* `Bug Tracker <http://github.com/immobiliare/sentry-php/issues>`_
* `Code <http://github.com/immobiliare/sentry-php>`_
