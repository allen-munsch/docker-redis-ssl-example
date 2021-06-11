## docker redis v6 with ssl example

```
# optionally create some new self signed certs
cd redis
bash gen-redis-cert.sh
cd ../

# using the base image layer in the redis/tls cert directory
docker build -t example/redis:v6.0.13 -f ./redis/Dockerfile ./

# start redis with ssl see: docker-redis-entrypoint.sh
docker-compose up
```
