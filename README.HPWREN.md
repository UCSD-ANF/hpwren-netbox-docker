# HPWREN-enhanced build of netboxcommunity/netbox container

See: [https://github.com/netbox-community/netbox-docker/wiki/Build#enhance-the-image]
See: [https://github.com/netbox-community/netbox-docker/wiki/Using-Netbox-Plugins]

Additional plugins in plugin_requirements.txt

## HOW TO RUN

### Devel

```bash
docker compose pull
docker compose build
docker compose up -d
```

### Production

```bash
docker compose pull
docker compose build
docker compose -f docker-compose.yml -f docker-compose.prod.yml up -d
```

## Build

### Default version

```bash
docker-compose build netbox

```

### Specific version

```bash
export VERSION=v3.2.5
docker-compose build --build-arg VERSION=v3.2.5 netbox

docker image tag gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:v3.2.5-plugins gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:v3.2-plugins

docker image tag gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:v3.2.5-plugins gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:latest-plugins

docker image push gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:v3.2.5-plugins
docker image push gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:v3.2-plugins
docker image push gitlab.hpwren.ucsd.edu:5005/systems/netbox-docker:latest-plugins
```
