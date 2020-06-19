# vcli

You can use a docker image for load vcli.

notice of usage of vcli on https://www.pgcli.com/

# Usage

You can use vcli 

```
docker run --rm -it -v <YourHome>:/in dbcliorg/vcli -h localhost -U dbadmin -W -p 5433 mydb
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/vcli -v <YourHome>:/in dbcliorg/vcli -h localhost -U dbadmin -W -p 5433 mydb
```

You can use alias

On linux

```
alias vcli="docker run --rm -it -v <YourHome>:/in dbcliorg/vcli"
vcli -h localhost -U dbadmin -W -p 5433 mydb
```

On Windows

```
@doskey vcli=docker run --rm -it -v <YourHome>:/in  dbcliorg/vcli
vcli -h localhost -U dbadmin -W -p 5433 mydb
```