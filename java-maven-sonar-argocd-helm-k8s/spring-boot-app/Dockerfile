FROM eclipse-temurin:17-jre-jammy

ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

RUN apt-get update \
    && apt-get install -y --only-upgrade \
        curl \
        libcurl4 \
        openssl \
        libssl3 \
    && rm -rf /var/lib/apt/lists/*

COPY ${artifact} app.jar

ENTRYPOINT ["java", "-jar", "app.jar"]