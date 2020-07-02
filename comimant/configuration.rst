Configuration
=============

The PM2 Ecosystem file can contain the following properties in the `env` object:

- `NODE_ENV` (required): Set to `development` for more detailed error messages, otherwise set to `production`.
- `PORT` (required): The port number of your Comimant installation.
- `CONFIG_FILE` (optional): Location to your Comimant configuration file. Can be relative to the Comimant root or absolute. Defaults to `config.json`.
- `DB_HOST` (required): Hostname of the MySQL server.
- `DB_PORT` (required): Port of the MySQL server.
- `DB_DATABASE` (required) The database to use.
- To be continued...