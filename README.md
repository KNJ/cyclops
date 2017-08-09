# Cyclops

## Getting Started

### Project

Make your project directory and public directory:

```sh
git clone git@github.com:KNJ/cyclops.git
cd cyclops
mkdir -p ./project/public
```

Create index file into the public directory:

```sh
echo "<?php phpinfo();" > ./project/public/index.php
```

### nginx-proxy

Make sure [nginx-proxy](https://github.com/jwilder/nginx-proxy) is running.

If not, nginx-proxy should be started first:

```sh
docker run -d -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy
```

### Docker Compose

Copy `.env.example` and save as `.env`:

```sh
cp .env.example .env
```

Run the containers and access http://localhost

```sh
docker-compose up -d
```
