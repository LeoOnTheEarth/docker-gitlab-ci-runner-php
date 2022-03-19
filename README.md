Docker GitLab CI Runner for PHP
===============================

Support PHP versions:

- PHP 5.4: `leoontheearth/docker-gitlab-ci-runner-php:5.4`
- PHP 5.5: `leoontheearth/docker-gitlab-ci-runner-php:5.5`
- PHP 5.6: `leoontheearth/docker-gitlab-ci-runner-php:5.6`
- PHP 7.0: `leoontheearth/docker-gitlab-ci-runner-php:7.0`
- PHP 7.1: `leoontheearth/docker-gitlab-ci-runner-php:7.1`
- PHP 7.2: `leoontheearth/docker-gitlab-ci-runner-php:7.2`
- PHP 7.3: `leoontheearth/docker-gitlab-ci-runner-php:7.3`
- PHP 7.4: `leoontheearth/docker-gitlab-ci-runner-php:7.4`
- PHP 8.0: `leoontheearth/docker-gitlab-ci-runner-php:8.0`
- PHP 8.1: `leoontheearth/docker-gitlab-ci-runner-php:8.1`

## Run Containers

```bash
docker run -t -i --rm -v /root/.composer:/root/.composer leoontheearth/docker-gitlab-ci-runner-php:7.2 bash
```

## Build Images

```bash
cd /tmp
git clone https://github.com/LeoOnTheEarth/docker-gitlab-ci-runner-php.git
cd docker-gitlab-ci-runner-php

docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:8.1 -f Dockerfile_81 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:8.0 -f Dockerfile_80 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:7.4 -f Dockerfile_74 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:7.3 -f Dockerfile_73 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:7.2 -f Dockerfile_72 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:7.1 -f Dockerfile_71 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:7.0 -f Dockerfile_70 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:5.6 -f Dockerfile_56 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:5.5 -f Dockerfile_55 ./
docker build --rm -t leoontheearth/docker-gitlab-ci-runner-php:5.4 -f Dockerfile_54 ./
```
