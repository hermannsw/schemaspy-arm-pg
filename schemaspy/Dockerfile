FROM arm64v8/openjdk:21-jdk-bullseye

ENV TZ=Asia/Tokyo
ENV DRIVER_URL https://repo1.maven.org/maven2/org/postgresql/postgresql/42.2.22/postgresql-42.2.22.jar
ENV APP_URL https://github.com/schemaspy/schemaspy/releases/download/v6.1.0/schemaspy-6.1.0.jar

WORKDIR /app

RUN apt-get update -y
RUN apt-get install -y graphviz tzdata wget libssl-dev fonts-liberation fonts-dejavu
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    wget -O postgresql-connector-java.jar ${DRIVER_URL} && \
    wget -O schemaspy.jar ${APP_URL}
