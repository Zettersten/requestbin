Originally Created by [Jeff Lindsay](http://progrium.com)

License
-------
MIT

## Deploy your own instance using Docker

On the server/machine you want to host this, you'll first need a machine with
docker and docker-compose installed, then grab the RequestBin source using git:

`$ git clone git@github.com:dotzero/requestbin.git`

Go into the project directory and then build and start the containers

```
$ sudo docker-compose build
$ sudo docker-compose up -d
```

Your own private RequestBin will be running on this server.


Contributors
------------
 * Barry Carlyon <barry@barrycarlyon.co.uk>
 * Jeff Lindsay <progrium@gmail.com>
