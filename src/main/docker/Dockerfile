FROM tomcat:8.0-jre8
MAINTAINER Eiffel-Community

ARG URL
RUN echo Building Eiffel-Intelligence Front-end image based on artifact url: ${URL}

# Create image with existing war file. User need to execute 'mvn package -DskipTest' before 'docker build'
RUN ["rm", "-fr", "/usr/local/tomcat/webapps/ROOT"]
ADD ${URL} /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
