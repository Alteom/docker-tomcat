FROM ubuntu:12.04
RUN apt-get update && apt-get upgrade -y && apt-get install -y openjdk-6-jre wget

ENV TOMCAT_VERSION 6.0.35
RUN wget https://archive.apache.org/dist/tomcat/tomcat-6/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz
RUN tar xzf apache-tomcat-$TOMCAT_VERSION.tar.gz

ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
#RUN mkdir -p "$CATALINA_HOME"

RUN mv apache-tomcat-$TOMCAT_VERSION /usr/local/tomcat

WORKDIR $CATALINA_HOME

EXPOSE 8080
CMD ["catalina.sh", "run"]