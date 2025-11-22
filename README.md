For windows: use build-run.ps1

In other cases:
docker compose down
docker compose build
docker-compose up config-service -d
sleep 5
curl http://localhost:8888/actuator/health
docker-compose up eureka-service -d
sleep 5
curl http://localhost:8761/actuator/health
docker-compose up -d
