#FROM openjdk:8-jdk-alpine
FROM frolvlad/alpine-oraclejdk8:slim
ENV JAVA_OPTS=""
VOLUME /tmp
COPY target/react-bff-*.jar app.jar
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -Dspring.profiles.active=docker -Djava.security.egd=file:/dev/./urandom -jar /app.jar"]
