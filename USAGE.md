## Quickstart
Using docker-compose
```
cd scripts/usage

// create a common network
docker network create common

// ipfs and mongodb
docker-compose -f data-layer-compose.yaml up -d

// start services
docker-compose -f services-compose.yaml up -d

// to stop
docker-compose -f <FILE> down // start services
```

## Dev Setup
```
cd scripts/setup
./clone.sh
./genproto.sh
```

Any changes to data lib project will have to be pushed along with a tag which has to be updated in other projects to use.

To build and run project individual services using docker:

```
1. create the common network as shown above
2. Assuming the data layer compose is up

3.
// to build image and run, "bo" argument to only build 
cd <service-folder>
./start.sh br
OR
// to run
cd <service-folder>
./start.sh
```
