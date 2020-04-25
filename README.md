Docker-compose for Penguin
==========================

## How to use

```
git clone http://github.com/tanupoo/penguin-docker.git
cd penguin-docker
```

Run the penguin service.
Note that the penguin service will be exposed to the open network by default.

```
docker-compose build
docker-compose up -d
```

Open your browser anywhere, and connect to the service like below.
If you have installed the containers in your local PC,
*YOUR_HOST_ADDRESS* can be replaced into *127.0.0.1*

```
http://YOUR_HOST_ADDRESS:8981
```

If you don't want to expose the service to the open network,
you have to change the variable PENGUIN_PORT in the .env file like below.

```
cat PENGUIN_PORT=127.0.0.1:8981 > .env
```

Then, restart the containers if needed.

```
docker-compose restart
```

If you have any trouble, the logging message may help you.

```
docker-compose logs -f
```

