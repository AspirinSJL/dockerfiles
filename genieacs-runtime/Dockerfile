FROM aspirinsjl/genieacs

# GenieACS will be listening to 0.0.0.0:7547
EXPOSE 7547

# Learn from truongsinh/nodejs-mongodb-redis
CMD mongod --fork -f /etc/mongod.conf && \
    redis-server /etc/redis/redis.conf && \
    genieacs-cwmp && \
    bash