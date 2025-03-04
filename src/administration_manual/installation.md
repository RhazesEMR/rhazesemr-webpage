# Dependencies

- Podman or Docker

# Database & API Installation

After saving the following compose file in a file named `docker-compose.yml` inside an empty directory, run `podman compose up -d` or `docker compose up -d`.

```yml
services:
  rhazesemrdb:
    container_name: rhazesemrdb
    image: ghcr.io/rhazesemr/rhazesemr-database:test
    environment:
      POSTGRES_PASSWORD: admin
      POSTGRES_DB: rhazesemrdb
      DATABASE_URL: postgres://postgres:admin@127.0.0.1:5432/rhazesemrdb
    volumes:
      - data:/var/lib/postgresql/data
    networks:
      - internal
    healthcheck:
      test: ["CMD", "pg_isready", "-U", "postgres"]
      interval: 5s
      timeout: 5s
      retries: 5

  rhazesemr-api:
    container_name: rhazesemr-api
    image: ghcr.io/rhazesemr/rhazesemr-api:test
    environment:
      DATABASE_URL: postgres://postgres:admin@rhazesemrdb:5432/rhazesemrdb
    ports:
      - "8808:3000"
    depends_on:
      rhazesemrdb:
        condition: service_healthy
    networks:
      - internal
      - external

  # oauth2:
  #   image: <oauth2_provider_image>
  #   ports:
  #     - "8080:8080"
  #   networks:
  #     - external

volumes:
  data:

networks:
  internal:
    internal: true
  external:
```

This will pull images containing both the API and the Database. The endpoint of the API will be running at port `3000` by default, and it will be accessible for all the devices sharing the same network as the device running the API. However, the database will be running in privet network that's only accessible from the machine running it. 

## Running Pre-configured Migrations

After setting up the database and the API, running this command will execute the pre-built binary provided in the container image.

```bash
podman exec -it rhazesemrdb db-migrator

# or if using Docker
docker exec -it rhazesemrdb db-migrator
```
