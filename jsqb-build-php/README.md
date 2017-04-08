# Environment
This docker is to build php7 and related tools.

* php7.0 php7.0-imagick php7.0-mongodb php7.0-redis
* rsync 3.1.0+
* git 1.9.1+
* composer 1.4.1+

From image ubuntu:14.04

## Build image

```bash
docker build -t cs17899219/jsqb-build-php:1.0 .
```

If building fail you can debug via where `1b372b1f76f2` is partial build

```bash
docker run --tty --interactive --rm 1b372b1f76f2 /bin/bash
```

Remove stoped container
```
docker rm $(docker ps -q -f status=exited)
```
