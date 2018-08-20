# docker-openresty-concat
nginx+openresty+concat


# docker

docker pull tinydever/docker-openresty-concat

# docker-composer

docker-composer up -d

```
version: "2"
services:
  web:
    restart: always
    image: tinydever/docker-openresty-concat
    ports:
      - "80:80"
    volumes:
      - ./conf/conf.d:/etc/openresty/nginx/conf.d
      - ./conf/nginx.conf:/etc/openresty/nginx/nginx.conf
      - ./log:/var/log/nginx
    networks:
      - code-network-openresty

```
