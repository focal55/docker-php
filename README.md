# PHP Apache

A [Docker](http://docker.com) container to run [PHP](http://php.net/) served from
 [Apache](https://httpd.apache.org/).
 
This image is based on the [Official PHP image](https://hub.docker.com/_/php/) with the addition
of some php extensions and mod rewrite enabled.

## Usage

To run the container, mount your application to `/var/www/html`.

Below is a [Docker Compose](https://docs.docker.com/compose/) example configuration:

```
web:
  image: thinkbean/php:7.1-apache
  links:
    - db
  ports:
    - "8000:80"
  volumes:
    - ./docroot:/var/www/html
```
