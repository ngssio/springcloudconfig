FROM openjdk:8-jdk-alpine
WORKDIR /opt/app
ARG JAR_FILE=./target/vdfconfigserver.jar
ARG PROP_FILE=./src/main/resources/application.properties
COPY ${JAR_FILE} app.jar
COPY ${PROP_FILE} application.properties
USER root
ENTRYPOINT ["java","-jar","app.jar","-Dspring.config.location=application.properties"]
