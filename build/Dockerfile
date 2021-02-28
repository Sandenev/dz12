FROM ubuntu:20.04
RUN apt-get update
RUN apt-get install git -y
RUN apt-get install default-jdk -y
RUN apt-get install maven -y
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample
WORKDIR /App42PaaS-Java-MySQL-Sample
RUN mvn package