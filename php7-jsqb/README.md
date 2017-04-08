# php7 phpunit and composer

This docker is to build php7 and related tools.

From image php:7.0

## Build image

```bash
docker build -t cs17899219/php7-composer-phpunit .
```

If building fail you can debug via where `1b372b1f76f2` is partial build

```bash
docker run --tty --interactive --rm 1b372b1f76f2 /bin/bash
```
