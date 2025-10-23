# backend/Dockerfile
FROM eclipse-temurin:17-jdk-jammy AS build
WORKDIR /workspace
COPY services/api/mvnw .
COPY services/api/.mvn .mvn
COPY services/api/pom.xml .
RUN ./mvnw -B -q dependency:go-offline

COPY services/api/src src
RUN ./mvnw -B -DskipTests package

FROM eclipse-temurin:17-jre-jammy
WORKDIR /app
ARG JAR_FILE=services/api/target/*.jar
COPY --from=build /workspace/${JAR_FILE} app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/app/app.jar"]
