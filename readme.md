
# Run
cd service1/
./mvnw spring-boot:run -Dspring-boot.run.arguments="--LOKI_HOST=http://localhost:3100/loki/api/v1/push"

cd service2/
./mvnw spring-boot:run -Dspring-boot.run.arguments="--LOKI_HOST=http://localhost:3100/loki/api/v1/push"

Start
``` bash
docker compose up -d  loki grafana
```

Stop and remove
```bash
docker compose down -v
```
# URLS


Graphana
http://localhost:3000/


# Testing
## Consul
curl http://localhost:8080/service1/hello

curl http://localhost:8081/service2/hello