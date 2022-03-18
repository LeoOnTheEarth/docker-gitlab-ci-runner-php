Docker GitLab CI Runner for PHP
===============================

Support PHP 5.4, 5.5, 5.6, 7.0, 7.1, 7.2

- PHP 5.4: `leoontheearth/docker-gitlab-ci-runner-php:5.4`
- PHP 5.5: `leoontheearth/docker-gitlab-ci-runner-php:5.5`
- PHP 5.6: `leoontheearth/docker-gitlab-ci-runner-php:5.6`
- PHP 7.0: `leoontheearth/docker-gitlab-ci-runner-php:7.0`
- PHP 7.1: `leoontheearth/docker-gitlab-ci-runner-php:7.1`
- PHP 7.2: `leoontheearth/docker-gitlab-ci-runner-php:7.2` (latest)

## Run Containers

```bash
docker run -t -i --rm -v /root/.composer:/root/.composer leoontheearth/docker-gitlab-ci-runner-php bash
```

## Build Image

```bash
cd /tmp
git clone https://github.com/LeoOnTheEarth/docker-gitlab-ci-runner-php.git
# Build for PHP 7.2
docker build -t leoontheearth/docker-gitlab-ci-runner-php:7.2 /tmp/docker-gitlab-ci-runner-php/7.2
```
