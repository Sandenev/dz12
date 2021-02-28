FROM ubuntu:20.04
RUN apt-get update
ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Europe/Moscow
RUN apt-get install -y tzdata
RUN apt-get install git -y
RUN apt-get install default-jdk -y
RUN apt-get install maven -y
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample
WORKDIR /App42PaaS-Java-MySQL-Sample
RUN mvn package