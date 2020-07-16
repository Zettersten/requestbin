Originally Created by [Jeff Lindsay](http://progrium.com)

## Deploy your own instance using Docker Hub

On the server/machine you want to host this, you'll first need a machine with
docker and docker-compose installed, create file `docker-compose.yml` contains:

```yaml
version: "3"
services:
  requestbin:
    image: dotzero/requestbin
    environment:
      REALM: prod
      REDIS_URL: "//redis:6379"
    links:
      - redis
    ports:
      - "8000:8000"

  redis:
    image: redis
```

After that, you could run it with:

```sh
$ sudo docker-compose up -d
```

## Build your own instance using Docker

On the server/machine you want to host this, you'll first need a machine with
docker and docker-compose installed, then grab the RequestBin source using git:

`$ git clone https://github.com/zero-sec/requestbin.git`

Go into the project directory and then build and start the containers

```sh
$ sudo docker-compose build
$ sudo docker-compose up -d
```

Your own private RequestBin will be running on this server.

Contributors
------------
* Barry Carlyon <barry@barrycarlyon.co.uk>
* Jeff Lindsay <progrium@gmail.com>

License
-------
MIT
