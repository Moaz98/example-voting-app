# -------- Stage 1: Build --------
FROM maven:3.5-jdk-8-alpine AS builder

WORKDIR /code
COPY . .
RUN mvn package -DskipTests

# -------- Stage 2: Runtime --------
FROM eclipse-temurin:8-jre-alpine

WORKDIR /app

COPY --from=builder /code/target/worker-jar-with-dependencies.jar /app/app.jar

CMD ["java", "-jar", "app.jar"]
