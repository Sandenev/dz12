FROM adoptopenjdk/openjdk11:alpine-slim
RUN apk update
RUN apk add wget
ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
RUN mkdir -p "$CATALINA_HOME"
WORKDIR $CATALINA_HOME
RUN wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.43/bin/apache-tomcat-9.0.43.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-9.0.43/* /usr/local/tomcat/
RUN mkdir /usr/local/tomcat/webapps/ROOT/
WORKDIR /usr/local/tomcat/webapps/
COPY ./Config.properties /usr/local/tomcat/webapps/ROOT
EXPOSE 8080
CMD ["catalina.sh", "run"]