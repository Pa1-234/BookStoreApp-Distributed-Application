FROM openjdk:8-jdk-alpine

VOLUME /tmp

ARG JAR_FILE=target/bookstore-account-service-0.0.1-SNAPSHOT.jar

COPY ${JAR_FILE} app.jar

#Using Dockerize to check whether the database is up, if it is, then start this service.
COPY dockerize /dockerize

CMD ["./dockerize", "-wait", "tcp://bookstore-mysql-db:3306", "-timeout", "15m", "java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar"]
