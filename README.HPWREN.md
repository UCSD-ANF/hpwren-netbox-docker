HPWREN-enhanced build of netboxcommunity/netbox container
========================

See: https://github.com/netbox-community/netbox-docker/wiki/Build#enhance-the-image
See: https://github.com/netbox-community/netbox-docker/wiki/Using-Netbox-Plugins

Additional plugins in plugin_requirements.txt

#HOW TO RUN

## Devel
docker-compose fetch
docker-compose build
docker-compose up -d

## Production
docker-compose fetch
docker-compose build
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d

