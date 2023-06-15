FROM maven as build
WORKDIR /app
COPY . .
RUN mvn install

FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=build /app/target/spring-boot-starter-parent-2.3.8.RELEASE.jar .
EXPOSE 9999
CMD [ "java","-jar","spring-boot-starter-parent-2.3.8.RELEASE.jar"]