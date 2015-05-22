FROM aspirinsjl/genieacs

# Learn from truongsinh/nodejs-mongodb-redis
CMD mongod --fork -f /etc/mongod.conf && \
    redis-server /etc/redis/redis.conf && \
    genieacs-cwmp && \
    bash