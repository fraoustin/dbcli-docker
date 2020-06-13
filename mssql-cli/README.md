# mssql-cli

You can use a docker image for load mssql-cli.

notice of usage of mssql-cli on https://github.com/dbcli/mssql-cli/


## Usage

You can use pgcli

```
docker run --rm -it dbcliorg/mssql-cli:1.0.0 -S <server URL> -d <database name> -U <username> -P <password>
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/pgcli dbcliorg/pgcli:3.0.0 -S <server URL> -d <database name> -U <username> -P <password>
```
