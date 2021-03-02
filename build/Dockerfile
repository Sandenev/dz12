FROM ubuntu:20.04
RUN apt-get update
ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Europe/Moscow
RUN apt-get install -y tzdata
RUN apt-get install git -y
RUN apt-get install default-jdk -y
RUN apt-get install maven -y
WORKDIR /home/user
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample
WORKDIR /home/user/App42PaaS-Java-MySQL-Sample
RUN echo "app42.paas.db.username = 42db_user" > WebContent/Config.properties
RUN echo "app42.paas.db.port = 3306" >> WebContent/Config.properties
RUN echo "app42.paas.db.password = secpass" >> WebContent/Config.properties
RUN echo "app42.paas.db.ip = database" >> WebContent/Config.properties
RUN echo "app42.paas.db.name = 42db" >> WebContent/Config.properties
RUN mvn package