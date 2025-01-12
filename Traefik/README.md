# README

This config is based on [Christian Lempas boiler plate](https://github.com/ChristianLempa/boilerplates/tree/main/docker-compose/traefik)

## Notes

### Frontend network

The network `frontend` is externally managed, and not automatically created when running `docker compose up`

To create the network, run the command

``` shell
# Create network
docker network create frontend

# Veriy that network `frontend` has been created
docker network ls
```
