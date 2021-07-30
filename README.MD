# Docker + nginx + mysql + php + adminer

Basic set for creating web-applications.

includes:
- php-fpm
- mysql
- nginx
- adminer

nginx :8000 http://localhost:8000

adminer :8080 http://localhost:8080/?server=mysql&username=test

**mysql:**
  - host: mysql
  - login: test
  - password: test


## Usage

```
clone project from console, and first start docker:

$ git clone https://github.com/klepatskiy/docker-nginx-php-mysql-adminer.git
$ cd docker-nginx-php-mysql-adminer
$ docker-compose up --build

All done. 
Open browser http://localhost:8000

Edit index.php, in current directory.

Edit database: http://localhost:8080/?server=mysql&username=test

```

**Useful commands**

First start docker 

```sh
docker-compose up --build
```

start docker
```sh
docker-compose up
```

list container
```sh
docker ps
```

Stop docker
```sh
docker-compose down
```
