FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

COPY pom.xml .
COPY src ./src

RUN ./mvnw -q -e -DskipTests package || mvn -DskipTests package

EXPOSE 8000

CMD ["java", "-jar", "target/payment-gateway-0.0.1-SNAPSHOT.jar"]
