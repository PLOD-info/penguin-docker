Docker-compose for Penguin
==========================

Note that the penguin service by this containers will be exposed to the open network by default.  See below if you want to change it.

## How to use

```
git clone http://github.com/tanupoo/penguin-docker.git
cd penguin-docker
```

Run the penguin service.

```
docker-compose build --pull
docker-compose up -d
```

Open your browser anywhere, and connect to the service like below.
If you have installed the containers in your local PC,
*YOUR_HOST_ADDRESS* can be replaced into *127.0.0.1*

```
http://YOUR_HOST_ADDRESS:8981
```

If you want to stop the service, type blow.

```
docker-compose down
```

All data are stored into the db directory.
Hence, they are remained after you stop the service.
You can reuse is later.

## Stop to expose the penguin service to the open network.

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

