Pinterest
---------

The provider uses the Pinterest API v5. For information on authentication, see:

    https://developers.pinterest.com/docs/getting-started/authentication/

You can optionally specify additional permissions to use. If no ``SCOPE``
value is set, the provider uses the ``user_accounts:read`` scope.

.. code-block:: python

    SOCIALACCOUNT_PROVIDERS = {
        "pinterest": {
            "SCOPE": ["user_accounts:read"],
        }
    }

SCOPE:
    For a full list of scope options, see

    https://developers.pinterest.com/docs/getting-started/scopes/
