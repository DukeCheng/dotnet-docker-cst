ARG REPO=mcr.microsoft.com/dotnet/core/aspnet
FROM $REPO:3.1.4

# Set apt repository to ustc
RUN curl --output /etc/apt/sources.list https://mirrors.ustc.edu.cn/repogen/conf/debian-http-4-buster \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
	apt-utils \
	libgdiplus \
	libc6-dev \
	net-tools \
	dnsutils \
	iputils-ping \
	telnet \
    && rm -rf /var/lib/apt/lists/* \
    && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo 'Asia/Shanghai' >/etc/timezone

