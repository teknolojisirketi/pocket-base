FROM alpine:latest

ARG PB_VERSION=0.30.0

RUN apk add --no-cache \
    unzip \
    ca-certificates \
    curl \
    bash

# Download and unzip PocketBase
ADD https://github.com/pocketbase/pocketbase/releases/download/v${PB_VERSION}/pocketbase_${PB_VERSION}_linux_amd64.zip /tmp/pb.zip
RUN unzip /tmp/pb.zip -d /pb/ && rm /tmp/pb.zip

WORKDIR /pb

# Expose default port (info only)
EXPOSE 8090

# Use environment variable for port
ENV POCKETBASE_PORT=8090

# Start PocketBase using env variable
CMD ["sh", "-c", "/pb/pocketbase serve --http=0.0.0.0:$POCKETBASE_PORT"]
