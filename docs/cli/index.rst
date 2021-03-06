Command Line Usage
==================

Sentry installs a command line script under the name ``sentry``. This will allow you to
perform most required operations that are unachievable within the web UI.

For a list of commands, you can also use ``sentry help``, or ``sentry [command] --help``
for help on a specific command.

Builtin Commands
----------------

.. data:: init [config]

    Initializes the configuration file for Sentry.

    Defaults to ~/.sentry/sentry.conf.py

    ::

        sentry init /etc/sentry.conf.py

.. data:: start [services]

    Starts all background services.

    If services are passed, only starts the given services.

    ::

        sentry start --daemon

.. data:: stop [services]

    Stops all background services.

    If services are passed, only stops the given services.

.. data:: restart [services]

    Stops all background services.

    If services are passed, only restarts the given services.

.. data:: upgrade

    Performs any needed database migrations.

.. data:: cleanup

    Performs all trim operations based on your configuration.

.. data:: manage [command] [args]

    A wrapper around ``django-admin.py`` (aka ``manage.py``).

    ::

        sentry manage createsuperuser

