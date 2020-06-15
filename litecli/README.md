# litecli

You can use a docker image for load litecli.

notice of usage of litecli on https://www.pgcli.com/

# Usage

You can use litecli for read the database <YourHome>/mydatabase

```
docker run --rm -it -v <YourHome>:/in dbcliorg/litecli /in/mydatabase
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/litecli -v <YourHome>:/in dbcliorg/litecli /in/mydatabase
```

You can use alias

On linux

```
alias litecli="docker run --rm -it -v <YourHome>:/in dbcliorg/litecli"
litecli mydatabase
```

On Windows

```
@doskey litecli=docker run --rm -it -v <YourHome>:/in  dbcliorg/litecli
litecli mydatabase
```