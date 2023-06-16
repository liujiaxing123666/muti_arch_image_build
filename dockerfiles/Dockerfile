# paddleflow/ubuntu:latest-test1
FROM ubuntu:18.04
# unsupport latest in our pr-test cluster, it will be update to latest once cluster updated

ENV DEBIAN_FRONTEND=noninteractive
RUN echo "deb http://kr.archive.ubuntu.com/ubuntu focal main universe" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y tini  && ln /usr/bin/tini /sbin/tini
RUN apt-get install -y libfuse-dev fuse gcc automake autoconf libtool make
RUN apt-get install -y tzdata   && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN apt-get install -y glusterfs-server
RUN apt-get install nfs-kernel-server -y
RUN apt-get install -y fuse
RUN rm -rf /var/lib/apt/lists/*

