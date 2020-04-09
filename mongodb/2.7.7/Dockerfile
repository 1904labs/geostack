FROM debian:jessie

WORKDIR /usr/local/tools/

RUN apt-get update && apt-get install -y \
    curl \
 && rm -rf /var/lib/apt/lists/*


RUN curl http://downloads.mongodb.org/linux/mongodb-linux-x86_64-2.7.7.tgz?_ga=1.59602981.96328107.1462517112 > mongodb-linux-x86_64-2.7.7.tgz

RUN gzip -d mongodb-linux-x86_64-2.7.7.tgz
RUN tar -xvf mongodb-linux-x86_64-2.7.7.tar

ENV PATH=$PATH:/usr/local/tools/mongodb-linux-x86_64-2.7.7/bin

WORKDIR /data/db/

WORKDIR /

EXPOSE 27017
CMD ["mongod"]
