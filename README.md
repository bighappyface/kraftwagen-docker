# Docker for Kraftwagen

This project contains a Docker COmpose configuration to run Kraftwagen Drupal sites.

## Accessing MariaDB Server

```
docker run --rm -it --link vagrant_mariadb_1:server bitnami/mariadb mysql -h server -u drupal -pdrupal
```

## Running commands in PHP container

```
docker exec -it vagrant_drupal_1 sh -c "cd /app/build/profiles/kraftwagen_docker && vendor/bin/drush status"
```

## See logs of a given container

```
docker-compose logs mariadb
```