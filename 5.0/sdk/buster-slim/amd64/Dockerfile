ARG REPO=mcr.microsoft.com/dotnet/sdk
FROM $REPO:5.0.102-1-buster-slim-amd64

# Work around for broken dotnet restore
ADD http://ftp.us.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20210119_all.deb .
RUN dpkg -i ca-certificates_20210119_all.deb

RUN apt-get update && apt-get install -y \
	ca-certificates \
	&& update-ca-certificates \
	&& rm -rf /var/lib/apt/lists/*

