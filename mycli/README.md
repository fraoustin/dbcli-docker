# mycli

You can use a docker image for load mycli.

notice of usage of mycli on https://www.mycli.net/

# Usage

If you have not a mysql server you can run a server with docker

```
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d -p 3306:3306 mysql
```

You can use mycli

```
docker run --rm -it dbcliorg/mycli -h <YourIp> -P 3306 -u root -p my-secret-pw
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/mycli dbcliorg/mycli -h <YourIp> -P 3306 -u root -p my-secret-pw
```

You can use alias

On linux

```
alias mycli="docker run --rm -it dbcliorg/mycli"
mycli -h <YourIp> -P 3306 -u root -p my-secret-pw
```

On Windows

```
@doskey mycli=docker run --rm -it dbcliorg/mycli
mycli -h <YourIp> -P 3306 -u root -p my-secret-pw
```
