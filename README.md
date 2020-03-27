# beef-xss docker container

## BeEF docker container

Docker container for the project beef-xss : https://beefproject.com/.


## Run the container :

```
git clone https://github.com/NeuronAddict/beef-docker.git
cd beef-docker
docker-compose up
# enjoy
```

## Ports

By default, ports on docker-compose bind to localhost.

If you want expose ports, replace port section of docker-compose :

```
ports:
    - 3000:3000
    - 61985:61985
    - 61986:61986
```

IF you change port in docker-compose, chage it un config.yaml
