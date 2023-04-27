# paddleflow/ubuntu:test20230426_2
FROM ubuntu:latest
# unsupport latest in our pr-test cluster, it will be update to latest once cluster updated

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get install -y tini --no-install-recommends && ln /usr/bin/tini /sbin/tini
RUN apt-get install -y libfuse-dev fuse gcc automake autoconf libtool make --no-install-recommends
RUN apt-get install -y tzdata --no-install-recommends  && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime 
RUN apt-get install -y glusterfs-server --no-install-recommends
RUN apt-get install nfs-kernel-server -y --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*
