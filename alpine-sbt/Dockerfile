FROM openjdk:jdk-alpine

ENV sbt_version 1.2.7
ENV sbt_home /usr/local/sbt
ENV PATH ${PATH}:${sbt_home}/bin

# Install sbt
RUN apk add --no-cache --update bash bc wget && \
    mkdir -p "$sbt_home" && \
    wget -qO - "https://github.com/sbt/sbt/releases/download/v$sbt_version/sbt-$sbt_version.tgz" | tar xz -C $sbt_home --strip-components=1 && \
    apk del wget && \
    sbt sbtVersion
WORKDIR /app
