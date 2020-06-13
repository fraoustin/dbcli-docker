# pgcli

You can use a docker image for load pgcli.

notice of usage of pgcli on https://www.pgcli.com/


## Usage

If you have not a postgresql server you can run a server with docker

```
docker run --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

You can use pgcli

```
docker run --rm -it dbcliorg/pgcli:3.0.0 -h YourIP -p 5432 -U postgres -W 
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/pgcli dbcliorg/pgcli:3.0.0 -h YourIP -p 5432 -U postgres -W 
```
