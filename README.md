
#[WIP]

# VeryNginx Dockerfile


`A very powerful and friendly nginx base on lua-nginx-module( openresty ) which provide WAF, Control Panel, and Dashboards.`


ImageLayers : [![](https://badge.imagelayers.io/camil/verynginx:latest.svg)](https://imagelayers.io/?images=camil/verynginx:latest)


This repository contains **Dockerfile** of [VeryNginx](https://github.com/alexazhou/VeryNginx)


## Informations


* Based on alpine:3.3  [alpine:3.3](https://hub.docker.com/r/_/alpine/)
* Install [Docker](https://www.docker.com/)

## Installation


        docker pull camil/verynginx
        cd ~
        git clone https://github.com/camilb/docker-verynginx.git


## Build


For example, if you need to install [Extra Modules](https://openresty.org), edit the Dockerfile and than build-it.

		cd ~/docker-verynginx
        docker build --rm -t camil/verynginx .

# Usage


Remove or modify conf.d/domain.conf and conf.d/domain-ssl.conf to match your needs :


		cd ~/docker-verynginx
        docker run -d -v $PWD/conf.d:/etc/nginx/conf.d -p 80:80 -p 443:443 camil/verynginx
