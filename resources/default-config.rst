Default Configuration
=====================

Comimant config.json
--------------------

.. code-block:: json

    {
        "title": "Acme Intranet",
        "keywords": "acme intranet",
        "description": "Some description about the Acme Intranet",
        "email_domains": [
            "@acme.com"
        ],
        "domains": [
            {
                "root": {
                    "domain": "example.com"
                },
                "main": {
                    "domain": "www.example.com"
                },
                "static": {
                    "domain": "static.example.com"
                },
                "accounts": {
                    "domain": "accounts.example.com"
                },
                "auth": {
                    "domain": "auth.example.com"
                }
            }
        ],
        "plugins_dir": "/path/to/comimant/root/plugins"
    }

Comimant Server config.json
---------------------------

PM2 Ecosystem
-------------

.. code-block:: json

    {
        "apps": [
            {
                "script": "/path/to/comimant/app.js",
                "name": "comimant",
                "env": {
                    "NODE_ENV": "production",
                    "PORT": "[port number]",
                    "DB_HOST": "127.0.0.1",
                    "DB_PORT": "3306",
                    "DB_DATABASE": "comimant",
                    "DB_USER": "comimant_user",
                    "DB_PASS": "Some secure password",
                    "DB_USER_MODIFY": "comimant_modify_user",
                    "DB_PASS_MODIFY": "Another secure password",
                    "DB_USER_DELETE": "comimant_delete_user",
                    "DB_PASS_DELETE": "Yet another secure password",
                    "REDIS_HOST": "127.0.0.1",
                    "REDIS_PORT": "6379",
                    "PEPPER": "8 char string",
                    "SECRET_1": "64 char hex string",
                    "SECRET_2": "64 char hex string",
                    "COOKIE_SECRET": "64 char hex string",
                    "DATABASE_KEY": "32 char hex string"
                }
            }
        ]
    }