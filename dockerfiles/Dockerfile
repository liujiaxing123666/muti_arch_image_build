# paddleflow/ubuntu:18.04-base
FROM ubuntu:18.04
# unsupport latest in our pr-test cluster, it will be update to latest once cluster updated

ENV DEBIAN_FRONTEND=noninteractive
RUN echo "deb http://kr.archive.ubuntu.com/ubuntu focal main universe" >> /etc/apt/sources.list && \
apt-get update && \
apt-get install -y tini  && \
apt-get install -y libfuse-dev fuse gcc automake autoconf libtool make && \
apt-get install -y tzdata   && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
apt-get install -y glusterfs-server && \
apt-get install nfs-kernel-server -y && \
apt-get install -y fuse && \
rm -rf /var/lib/apt/lists/*
