# prisma-mongo-demo

## install mongo

* docker

```bash
// pull image
docker pull bitnami/mongodb:5.0

// container
docker run --name docker-mongo -e ALLOW_EMPTY_PASSWORD=yes -p 27017:27017 -d bitnami/mongodb:5.0
```

* docker-compose

```bash
docker-compose exec mongo mongo --eval "rs.initiate({_id: 'rs0', members: [{_id: 0, host: 'mongo:27017'}]});"
```

## usage

* generate

```bash
npx prisma generate
```

* migrate

```bash
npx prisma migrate status --schema=./prisma/schema.prisma
```
