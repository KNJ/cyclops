# Cyclops

## Setup Environment

### nginx-proxy

Make sure [nginx-proxy](https://github.com/jwilder/nginx-proxy) is running.

If not, nginx-proxy should be started first.

```sh
docker run -d -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy
```

### Docker Compose

Pass the following environment variables hen you run `docker-compose up`.

- `VIRTUAL_HOST`
- `MYSQL_ROOT_PASSWORD`
- `MYSQL_DEV_PASSWORD`
- `MYSQL_PORT`

```bash
env VIRTUAL_HOST=cyclops.wazly.net \
MYSQL_ROOT_PASSWORD=root_password \
MYSQL_DEV_PASSWORD=dev_password \
MYSQL_PORT=3306:3306 \
docker-compose up -d
```
