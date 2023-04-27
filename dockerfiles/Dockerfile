# paddleflow/ubuntu:latest
FROM ubuntu:latest
# unsupport latest in our pr-test cluster, it will be update to latest once cluster updated

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y tini --no-install-recommends && ln /usr/bin/tini /sbin/tini && \
    apt-get install -y libfuse-dev fuse gcc automake autoconf libtool make --no-install-recommends && \
    apt-get install -y tzdata --no-install-recommends  && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    apt-get install -y glusterfs-server --no-install-recommends && \
    apt-get install nfs-kernel-server -y --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*
RUN apt-get install meson -y --no-install-recommends && \
    apt-get install ninja-build -y --no-install-recommends && \
    apt install python3-pip -y --no-install-recommends && \
    pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple pytest --no-install-recommends && \
    apt-get install pkg-config -y --no-install-recommends && \
    apt-get install udev -y --no-install-recommends
