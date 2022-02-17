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
docker-compose up
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
