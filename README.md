Docker-compose for Penguin
==========================

## limitations

Currently, you can access to this container in your PC.
You can't use this containers remotely.

## How to use

```
git clone http://github.com/tanupoo/penguin-docker.git
```

```
cd penguin-docker
docker-compose up --build -d
```

open your browser and connect to the following address.

```
http://127.0.0.1:8981
```

If you have any trouble, the logging message may help you.

```
docker-compose logs -f
```

## TODO

- adding something level of security for user authentication with TLS.
- making containers for the on-premise version.
- making containers for the cloud version.

