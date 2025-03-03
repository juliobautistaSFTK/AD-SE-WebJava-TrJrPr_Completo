# Usa una imagen base con Java 8
FROM openjdk:8-jdk-alpine

# Instalar Maven
RUN apk update && apk add maven

# Instalar Tomcat 8.5+
RUN wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.0/bin/apache-tomcat-8.5.0.tar.gz && \
    tar -xvzf apache-tomcat-8.5.0.tar.gz && \
    mv apache-tomcat-8.5.0 /opt/tomcat

# Establecer variables de entorno
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk
ENV CATALINA_HOME=/opt/tomcat
ENV PATH=$JAVA_HOME/bin:$PATH:$CATALINA_HOME/bin
