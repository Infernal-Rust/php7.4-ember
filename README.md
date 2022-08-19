# php7.4-ember
[![CI](https://github.com/Infernal-Rust/php7.4-ember/workflows/CI/badge.svg)](https://github.com/Infernal-Rust/php7.4-ember/actions/workflows/ci.yml)

Docker container with all the requirements for Ember.

Based on `php7.4-apache`.

## Usage
Run the container with the Ember source files volumed to `/var/www/html`.
```
docker run \
  -itd \
  --name=ember \
  -p 80:80 \
  -v /path/to/ember/web:/var/www/html \
  php7.4-ember
```

The web files will need the following ownership set to work with the container.
```
chown 33:33 -R /path/to/ember/web
```
