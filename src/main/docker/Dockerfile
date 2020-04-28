FROM openjdk

RUN yum install -y java

VOLUME /tmp
ADD /maven/spring-boot-web-0.0.1-SNAPSHOT.jar myapp.jar
RUN sh -c 'touch /myapp.jar'
ENTRYPOINT ["java" , "-Djava.security.edg=file:dev/./urandom" , "-jar" , "myapp.jar"]