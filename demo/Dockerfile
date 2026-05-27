# FROM openjdk:21
FROM eclipse-temurin:21-jdk
COPY /target/MySprDockerApp.jar myapp.jar

EXPOSE 8080

ENTRYPOINT ["java","-jar","./myapp.jar"]
