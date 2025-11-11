FROM eclipse-temurin:21-jre
WORKDIR /app
COPY target/authentication-service-1.0.0.jar ./authentication-service.jar
EXPOSE 8081
CMD ["java", "-jar", "authentication-service.jar", "--server.port=8081"]