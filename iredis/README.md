# iredis

You can use a docker image for load iredis.

notice of usage of iredis on https://github.com/laixintao/iredis

# Usage

If you have not a redus server you can run a server with docker

```
docker run --name redis -p 6379:6379 --hostname=redis -d redis
```

You can use iredis

```
docker run --rm -it dbcliorg/iredis --url redis://<YourIp>:6379/1
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/iredis -v <YourHome>:/in dbcliorg/iredis --url redis://<YourIp>:6379/1
```

You can use alias

On linux

```
alias iredis="docker run --rm -it -v <YourHome>:/in dbcliorg/iredis"
iredis --url redis://<YourIp>:6379/1
```

On Windows

```
@doskey iredis=docker run --rm -it -v <YourHome>:/in  dbcliorg/iredis
iredis --url redis://<YourIp>:6379/1
```