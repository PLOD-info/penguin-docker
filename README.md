Docker-compose for Penguin
==========================

## How to use

```
git clone http://github.com/tanupoo/penguin-docker.git
```

```
cd penguin-docker
docker-compose build --force-rm mongo mongo-express penguin-docker
docker-compose up -d
```

```
docker-compose logs -f
```
