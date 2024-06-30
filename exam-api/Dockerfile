# 使用 Maven 镜像构建 Spring Boot 应用
FROM maven:3.8.1-openjdk-11 AS build
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests

# 使用 JRE 镜像运行 Spring Boot 应用
FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=build /app/target/*.jar app.jar

# 暴露端口
EXPOSE 8101

# 启动应用
CMD ["java", "-jar", "app.jar"]