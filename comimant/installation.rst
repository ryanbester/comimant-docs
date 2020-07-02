Installation
============

At the moment, Comimant can only be installed manually, but an automatic installation script is in development.

Automatic Installation
----------------------

In development.

Manual Installation
-------------------

These steps will show you how to get Comimant installed. It is assumed that you have configured your server with the necessary requirements, including a web server as a reverse proxy.

First of all, you will need to create a database for Comimant, along with some users. Open your MySQL shell and type the following commands.

.. code-block:: mysql

    /* Change this to what suits your needs */
    CREATE DATABASE comimant;

    /* Set a secure unique password for each user for maximum security */
    CREATE USER 'comimant_user'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
    CREATE USER 'comimant_modify_user'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
    CREATE USER 'comimant_delete_user'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

    /* Grant the necessary privileges */
    GRANT SELECT ON comimant.* to 'comimant_user'@'localhost';
    GRANT SELECT,INSERT,UPDATE,CREATE,REFERENCES,INDEX,ALTER ON comimant.* to 'comimant_modify_user'@'localhost';
    GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,REFERENCES,INDEX,ALTER ON comimant.* to 'comimant_delete_user'@'localhost';

    /* Flush the privileges */
    FLUSH PRIVILEGES;

Next, create a directory in your web server root for your Comimant site, this is typically in /var/www. Set your working directory to that directory, and create an html and static directory. Run `git clone https://github.com/ryanbester/comimant.git` to clone the Comimant source code into the comimant directory. Finally, move the assets directory from the comimant directory to the static directory to serve the static resources.

Now, install the dependencies by running `npm install` in the comimant directory. This may take a while depending on your server. For the configuration, create a config.json file in the comimant directory and an ecosystem.json file in your site root. See :doc:`/resources/default-config` for the default configuration.

Run `pm2 start ecosystem.json` to start Comimant for the first time. This will require you to create the database tables and a default user with admin privileges. To do this, go to [your site root]/setup in a web browser and follow the steps. Be sure to type your password carefully, since you won't be able to easily change if you make a mistake.