FROM aspirinsjl/nodejs

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv C7917B12 && \
    apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y redis-server && \
    apt-get clean 

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 && \
    echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list && \
    apt-get update && \
    apt-get install -y mongodb-org=3.0.3 mongodb-org-server=3.0.3 mongodb-org-shell=3.0.3 mongodb-org-mongos=3.0.3 mongodb-org-tools=3.0.3 && \
    echo "mongodb-org hold" | sudo dpkg --set-selections && \
    echo "mongodb-org-server hold" | sudo dpkg --set-selections && \
    echo "mongodb-org-shell hold" | sudo dpkg --set-selections && \
    echo "mongodb-org-mongos hold" | sudo dpkg --set-selections && \
    echo "mongodb-org-tools hold" | sudo dpkg --set-selections
