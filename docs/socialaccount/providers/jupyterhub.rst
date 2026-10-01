JupyterHub
----------

Documentation on configuring a key and secret key
    https://jupyterhub.readthedocs.io/en/stable/api/services.auth.html

Development callback URL
    http://localhost:800/accounts/jupyterhub/login/callback/

Specify the URL of your JupyterHub server as follows:

.. code-block:: python

    SOCIALACCOUNT_PROVIDERS = {
        'jupyterhub': {
            'API_URL': 'https://jupyterhub.example.com',
        }
    }

Usernames as account identifiers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The JupyterHub provider uses the username returned by the Hub as the account
identifier because the user endpoint does not provide a generic, stable
alternative. Ensure that your JupyterHub authenticator treats usernames as
immutable and never reassigns a former username to another user. Otherwise, a
new owner of a reassigned username could be matched to the previous owner's
local account.
