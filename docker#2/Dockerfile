FROM ubuntu:16.04
RUN set -ex && \
    cd /home/ && \
    apt update && \
    apt-get install -y tomcat8 git maven openjdk-8-jdk curl && \
    git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello boxfuse && \
    cd boxfuse/ && \
    mvn package && \
    cp ./target/hello-1.0.war /var/lib/tomcat8/webapps/
	  
EXPOSE 8080
  
CMD /usr/share/tomcat8/bin/catalina.sh run
