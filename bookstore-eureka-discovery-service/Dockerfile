# Use an official OpenJDK runtime as a parent image
FROM openjdk:8-jdk-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Build your application with Maven (assuming you have a Maven Wrapper)
#RUN ./mvnw clean install -DskipTests

# Make port 8761 available to the world outside this container
EXPOSE 8761

# Run your application using the JAR file
CMD ["java", "-jar", "target/bookstore-eureka-discovery-service-0.0.1-SNAPSHOT.jar"]
