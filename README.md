# BGP Simulator: A Mini Internet

## Setup
### Build docker container
- BGP Webserver
```
# build and tag docker image
docker build ./bgp-webserver -t bgp-webserver:latest
```

- BGP Router
```
# build and tag docker image
docker build ./bgp-router -t bgp-router:latest
```

## Run
### Run BGP Webserver (Standalone)
```
docker run -d --rm -p 8000:80 -p 8443:443 --name bgp-webserver-01 bgp-webserver:latest 
```

### Run BGP router (Standalone)
```
docker run -d --rm --name bgp-router-01 bgp-router:latest
```

### Run BGP Simulator
```
docker-compose up -d
```