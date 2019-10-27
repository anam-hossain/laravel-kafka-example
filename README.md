# laravel-kafka-example
Pub-Sub Messaging with Laravel and Apache Kafka

## Getting started

The quickest way to get started with the Bitnami Laravel Development Container is using [docker-compose](https://docs.docker.com/compose/).

Begin by creating a directory for your Laravel application:

```bash
mkdir ~/myapp
cd ~/myapp
```

Download the [docker-compose.yml](https://raw.githubusercontent.com/bitnami/bitnami-docker-laravel/master/docker-compose.yml) file in the application directory:

```bash
$ curl -LO https://raw.githubusercontent.com/bitnami/bitnami-docker-laravel/master/docker-compose.yml
```

Finally launch the Laravel application development environment using:

```bash
$ docker-compose up
```

Among other things, the above command creates a container service, named `myapp`, for Laravel development and bootstraps a new Laravel application in the application directory. You can use your favorite IDE for developing the application.

## Executing commands

Commands can be launched inside the `myapp` Laravel Development Container with `docker-compose` using the [exec](https://docs.docker.com/compose/reference/exec/) command.

> **Note**:
>
> The `exec` command was added to `docker-compose` in release [1.7.0](https://github.com/docker/compose/blob/master/CHANGELOG.md#170-2016-04-13). Please ensure that you're using `docker-compose` version `1.7.0` or higher.

The general structure of the `exec` command is:

```bash
$ docker-compose exec <service> <command>
```

, where `<service>` is the name of the container service as described in the `docker-compose.yml` file and `<command>` is the command you want to launch inside the service.

Following are a few examples of launching some commonly used Laravel development commands inside the `myapp` service container.

- List all `artisan` commands:

  ```bash
  $ docker-compose exec myapp php artisan list
  ```