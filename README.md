Docker container of PHP 5.2 with Apache
=======================================
* CentOS 5 
* Apache 2
* PHP 5.2
* PHP GD
* PHP PDO
    * MySQL (`mysql-devel`)
    * PostgreSQL (`postgresql-devel`)
    * Oracle 11g (Oracle Instant Client 11.2)
    * SQLite (`sqlite-devel`)


Oracle Instant Client

* [Oracle Instant Client Downloads](http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html)

* `oracle-instantclient11.2-basic-11.2.0.4.0-1.x86_64.rpm`
* `oracle-instantclient11.2-devel-11.2.0.4.0-1.x86_64.rpm`

```
docker build -t sonicjam/php-5.2-apache ./
```

```
docker run \
    -d \
    -p 49160:80 \
    -v ${HOME}:/data \
    -v ${PROJ_DIR}/htdocs:/var/www/html \
    sonicjam/php-5.2-apache
```
