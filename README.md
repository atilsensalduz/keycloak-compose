1. Requires [Docker](https://docs.docker.com/engine/install/) with [Compose](https://docs.docker.com/compose/install/)
2. Parameterized using variables in the [`.env`](./.env) file
3. Up the project using command:
```sh
docker compose up -d --wait
```

| Useful commands | Discription
|-|-
| `docker stats` | Containers resource usage (use `--no-stream` only pull the first result)
| `docker compose logs` | Shows logs of containers (use flag `-f` to follow logs)
| `docker compose down` | Stop and remove containers (flag `-v` remove named volumes declared in the volumes section of the Compose file and anonymous volumes attached to containers)
| `docker system prune -a -f` | Remove all unused containers, networks, images (flag `--volumes` prune volumes)

| App | Port | Username | Password | Image
|-|-|-|-|-
| Keycloak | 8080 | `admin` | `keycloak` | ![Keycloak Grafana Client in the realm test](./.github/images/keycloak.png)
| Prometheus | 9090 | | | ![Prometheus Targets](./.github/images/prometheus.png)
| Grafana | 3000 | `admin` | `grafana` | ![Grafana Keycloak Dashboard](./.github/images/grafana.png)
