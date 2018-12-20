
## This file has few main steps in the history file

## Spin up mids container
#### docker run -it --rm -v ~/w205:/w205 midsw205/base bash

## Create and negigate to redis-standalone
#### mkdir ~/w205/redis-standalone
#### cd ~/w205/redis-standalone

## In the same directory, copy example-0-docker-compose.yml into docker-compose.yml
#### cp ../course-content/05-Storing-Data-II/example-0-docker-compose.yml docker-compose.yml

## Spin up the redis container
#### docker-compose up -d

## Check the log redis
#### docker-compose ps
#### docker-compose logs redis
#### Ready to accept connections

## Open python
#### ipython

## Spin down the redis container and check the container, nother should be there
#### docker-compose down
#### docker-compose ps

## Create and negigate to redis-cluster
#### mkdir ~/w205/redis-cluster
#### cd redis-cluster

## In the same directory, copy example-1-docker-compose.yml into docker-compose.yml
#### cp ../course-content/05-Storing-Data-II/example-1-docker-compose.yml docker-compose.yml

## Change .yml file
#### version: '2'
#### services:

## Check the log redis
#### docker-compose logs redis

## Connect to mids container
#### docker-compose exec mids bash

## Spin it donw and check the contianer and nothing should be there
#### docker-compose down
#### docker-compose ps

## write to history
#### history > hong-history.txt
