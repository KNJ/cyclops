# Cyclops

## Setup Environment

### nginx-proxy

Make sure [nginx-proxy](https://github.com/jwilder/nginx-proxy) is running.

If not, nginx-proxy should be started first.

```sh
docker run -d -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy
```

### Docker Compose

Run the containers and access http://localhost

```sh
docker-compose up -d
```
