
# Restoring a redis backup
* Copy the rdb file into the redis directory
* Rename it to be `dump.rdb`
* `docker-compose up`
* to connect with redis-cli
  * on Mac: `redis-cli -h $(docker-machine ip) -p 3220`
  * on Linux: `redis-cli -h 127.0.0.1 -p 3220`

## Comments
* To change the port `3220` to any other port number change it in `docker-compose.yml`
* If no .rdb file is present, redis will only run in memory
* To create a backup file
 * grant permissions to the redis folder `chmod -R a+w redis/`
 * type `save` in redis-cli