# portainer

Portainer container management UI configuration

## Requirements

- Docker
- Docker compose

## Running

### Environment variables

Copy example file

```
cp .env.example .env
```

Fill in fields in `.env`

### Production mode

#### Run in docker swarm mode

```
docker stack deploy -c <(docker-compose -f docker-compose.yml -f docker-compose.prod.yml -f docker-compose.swarm.yml config) portainer
```

#### Run in docker compose mode

```
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d
```

### Development mode

#### Run in docker swarm mode

```
docker stack deploy -c <(docker-compose -f docker-compose.yml -f docker-compose.dev.yml -f docker-compose.swarm.yml config) portainer
```

#### Run in docker compose mode

```
docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d
```
