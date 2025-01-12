# Gitea Installation

This is pretty much line-for-line copied from Christian Lempa's [Gitea Boilerplate](https://github.com/ChristianLempa/boilerplates/blob/main/docker-compose/gitea/compose.yaml)

## Notes

This configuration uses Traefik as a Reverse Proxy, there should already be a Traefik instance running connected to the docker network `frontend`

This configuration also uses the port 2221 for ssh to Gitea, you could change the default SSH port on the server the container is running on, and map port 22 on the host, to port 22 in the container. There is really no functional difference as far as i'm aware.

## App.ini

Reason for splitting the configuration of Gitea out to a app.ini file is being done in order to have a minimal docker compose file. This makes it easier to reuse the docker compose template with an existing Gitea configuration. Only the most basic configuration settings will be done through the docker compose file.

Since all changes done to the config from the admin interface will be reflected in `custom/conf/app.ini`, this file can be mounted as Read-Only
