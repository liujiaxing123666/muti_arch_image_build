# paddleflow/ubuntu:test20230426_2
FROM ubuntu:latest
# unsupport latest in our pr-test cluster, it will be update to latest once cluster updated

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get install -y tini && ln /usr/bin/tini /sbin/tini
RUN apt-get install -y libfuse-dev fuse gcc automake autoconf libtool make
RUN apt-get install -y tzdata && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN apt-get install -y glusterfs-server
RUN apt-get install nfs-kernel-server -y
