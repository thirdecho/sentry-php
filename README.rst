immobiliare/sentry-php
======================

|Travis CI| |Latest Stable Version| |Total Downloads| |Latest Unstable Version|
|License| |Monthly Downloads| |Daily Downloads|

.. |Travis CI| image:: https://secure.travis-ci.org/getsentry/sentry-php.png?branch=master
:target: http://travis-ci.org/getsentry/sentry-php
.. |Latest Stable Version| image:: https://poser.pugx.org/immobiliare/sentry-php/v/stable
:target: https://packagist.org/packages/immobiliare/sentry-php
.. |Total Downloads| image:: https://poser.pugx.org/immobiliare/sentry-php/downloads
:target: https://packagist.org/packages/immobiliare/sentry-php
.. |Latest Unstable Version| image:: https://poser.pugx.org/immobiliare/sentry-php/v/unstable
:target: https://packagist.org/packages/immobiliare/sentry-php
.. |License| image:: https://poser.pugx.org/immobiliare/sentry-php/license
:target: https://packagist.org/packages/immobiliare/sentry-php
.. |Monthly Downloads| image:: https://poser.pugx.org/immobiliare/sentry-php/d/monthly
:target: https://packagist.org/packages/immobiliare/sentry-php
.. |Daily Downloads| image:: https://poser.pugx.org/immobiliare/sentry-php/d/daily
:target: https://packagist.org/packages/immobiliare/sentry-php

This project is a fork of official `PHP SDK v1.7 <https://github.com/getsentry/sentry-php>`_ for `Sentry <https://getsentry.com/>`_ to work even with php5.2.

Installation
------------

There are various ways to install the PHP integration for Sentry.  The
recommended way is to use `Composer <http://getcomposer.org/>`__::

    $ composer require immobiliare/sentry-php:1.7.x-dev

Alternatively you can manually install it:

1.  Download and extract the latest `sentry-php
    <https://github.com/immobiliare/sentry-php/archive/master.zip>`__ archive
    to your PHP project.
2.  Require the autoloader in your application:

    .. sourcecode:: php

        require_once '/path/to/Raven/library/Raven/Autoloader.php';
        Raven_Autoloader::register();


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
