FROM ubuntu:16.04

RUN cd /usr/local/ && mkdir tomcat && cd tomcat && mkdir webapps

RUN apt update && apt -y install git && \
    apt -y install maven && apt -y install default-jdk && \
    git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git && \
    cd boxfuse-sample-java-war-hello && mvn package

RUN apt clean

CMD cp /boxfuse-sample-java-war-hello/target/hello-1.0.war  /usr/local/tomcat/webapps/
