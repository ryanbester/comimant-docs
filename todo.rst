ToDo
====

.. |checked| raw:: html

    <input type="checkbox" disabled checked>

.. |unchecked| raw:: html

    <input type="checkbox" disabled>

This page will list what has been implemented in Comimant, and what is still being 
under development.

These are the core features, and Comimant will be released as soon as these have 
been implemented (alpha releases may be available before, but must not be installed
on production).

For additional features, open a new Feature Request issue on the Comimant or Comimant
Server GitHub repository. Some features may be able to be implemented in plugins. 
If this is the case, the feature will be postponed and marked as Unimportant.

Comimant
--------

Accounts
~~~~~~~~
- |checked| Login system
- |checked| User privileges
- |checked| Change name, username, and DOB
- |unchecked| Ability to manage other services
- |unchecked| View data usage (Comimant Server)

Security
~~~~~~~~
- |checked| Password encryption
- |unchecked| Password requirement enforcement
- |unchecked| 2 factor authentication
- |unchecked| Login with identity providers/SSO (e.g. SAML, AD)
- |unchecked| LDAP integration
- |checked| Access tokens
- |checked| Ability to log out everywhere
- |checked| Nonce system

Frontend
~~~~~~~~
- |checked| Widget system
- |unchecked| Customisable navigation bar
- |unchecked| Custom user pages
- |unchecked| User personalisation options (background colour, etc.)
- |unchecked| Notification system (e.g. webhooks)
- |unchecked| Global message broadcasting
- |unchecked| Files browser (Comimant Server)

Admin interface
~~~~~~~~~~~~~~~
- |checked| User management
- |checked| Privilege management
- |unchecked| Widget type management
- |unchecked| Access token management
- |unchecked| Nonce management
- |unchecked| Server data usage (Comimant Server)

Comimant Plugins
~~~~~~~~~~~~~~~~

- |checked| Basic plugin loader
- |unchecked| Core API

Comimant Server
---------------

Core
~~~~

- |unchecked| Request handling
- |unchecked| Protocol decoding

Protocol Security
~~~~~~~~~~~~~~~~~

- |unchecked| Packet encryption
- |unchecked| Authorisation

Comimant Server Plugins
~~~~~~~~~~~~~~~~~~~~~~~

- |unchecked| Plugin loader
- |unchecked| API

Features
~~~~~~~~

- |unchecked| Disk usage querying
- |unchecked| Drive querying
- |unchecked| System user management
- |unchecked| Backup management
- |unchecked| System monitoring
- |unchecked| File browsing