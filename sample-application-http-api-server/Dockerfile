# Run
FROM openjdk:11-jre
ENV MYAPP_HOME /sample-application-http-api-server/
WORKDIR $MYAPP_HOME
COPY $MYAPP_HOME/target/*.jar $MYAPP_HOMME/myapp.jar
ENTRYPOINT java -jar myapp.jar