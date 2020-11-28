# LEMP Server built using docker
## (and docker-compose)

Simply load your files into ``/src`` and run ``docker-compose up -d`` and away you go. 

### Changing NGINX config

The NGINX config can be fount at ``/dockerstuff/nginx/nginx.conf``, feel free to change it however you see fit!

### Modifying port

By default the app will expose itself on port ``8080``, if you want to change which port this is, you will need to change the following:

<pre>
services:
  nginx:
    ports:
      - "<b>8080</b>:80"
</pre>

### Changing PHP version

By default, the docker-compose file will load the latest PHP-FPM version from docker hub, simply change the following line to download a specific version of PHP:

<pre>
services:
  ...
  php:
    image: php:<b>7.4</b>-fpm
    ...
  ...
...
</pre>
