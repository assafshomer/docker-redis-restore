
# Restoring a redis backup
* Copy the rdb file into the redis directory
* Rename it to be `dump.rdb`
* `docker-compose up`
* `redis-cli -h 192.168.99.100 -p 3220`