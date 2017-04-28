# Nginx
Nginx is a lightweight, easy to configure host software and we recommend it for use together with nodejs and python.

## Positive
1. fast
1. stable
1. feature-rich
1. not as bloated as apache

## Negative
1. configuration

## Our approach at Lossless
Nginx is good and fast at what it does: handling traffic. The configuration should not be done manually though.
This is why we wrote coretraffic, a tool that handles configuration for you and even supports reverse config handling for docker clusters :) and automatic LetsEncrypt certificate retrieval.

## Watch and Learn

## Links to learn more

## Handy stuff

### nginx config for static content:
Here is a bestpractice standard config file that will serve the site/ directory of your project:

    server {

        listen *:80;
        server_name   ~^(www\.)?(?<domain>.+)$;
        rewrite        ^ https://$domain$request_uri permanent;
    }

    server {
        listen *:443 ssl;
        server_name   ~^(www\.)?(?<domain>.+)$;
        access_log /var/log/nginx/servezone.access.log;
        error_log /var/log/nginx/servezone.error.log;
        root /srv/www/$domain/site/;
        index index.html index.htm index.php;
        location  / {
        }
        location = /favicon.ico {
            log_not_found off;
            access_log off;
        }
        location = /robots.txt {
            allow all;
            log_not_found off;
            access_log off;
        }
        ssl_certificate /srv/ssl/newssl/server.crt;
        ssl_certificate_key /srv/ssl/newssl/server.key;
        location ~ /\.git {
            deny all;
        }
    }

### nginx with Docker
[Read on here](docker.md#nginxproxy) to get a neat nginx setup for docker containers.

### fix permissions of serving directory
this assumes that your nginx runs as user `www-data`
```sh
sudo chown -cR www-data:www-data /servingDir/
```