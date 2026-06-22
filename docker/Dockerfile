FROM maven:3.9-eclipse-temurin-17 AS BUILDER

WORKDIR /build 

COPY app/ .

RUN mvn clean package -DskipTests -Dmaven.gitcommitid.skip=true

FROM eclipse-temurin:17-jre AS RELEASE

WORKDIR /app

COPY --from=BUILDER /build/target/*.jar app.jar

ENTRYPOINT ["java", "-jar", "app.jar"]

