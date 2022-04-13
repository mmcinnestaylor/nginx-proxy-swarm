# nginx-proxy-swarm
This Docker Swarm service implements [nginx-proxy/nginx-proxy](https://github.com/nginx-proxy/nginx-proxy) using the 3 container setup of [nginx-proxy/acme-companion](https://github.com/nginx-proxy/acme-companion). A [helderco/docker-gen](https://github.com/helderco/docker-gen) image is used in place of a [nginx-proxy/docker-gen](https://github.com/nginx-proxy/docker-gen) image, as the latter does not support dynamic container names.

This deployment works in a single node swarm and uses the [Docker local volume driver](https://docs.docker.com/storage/volumes/). Multi-node swarms should use a different driver to enable volume persistence across nodes. 
