FROM maven:3.6.3-openjdk-11  as build
LABEL author="venkat"
WORKDIR /app
RUN git clone https://github.com/spring-projects/spring-petclinic.git && cd spring-petclinic/ && mvn clean package


FROM tomcat:8.5.81-jre8
EXPOSE 80
COPY --from=build /app/spring-petclinic/target/spring-petclinic-2.7.0-SNAPSHOT.jar /usr/local/tomcat/webapps/spring-petclinic-2.7.0-SNAPSHOT.jar
CMD ["catalina.sh", "run"]




