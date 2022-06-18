FROM ubuntu:22.04

RUN apt update
RUN apt install -y wget unzip

RUN mkdir atm6
RUN wget https://media.forgecdn.net/files/3814/820/ATM6-1.8.26-server.zip && \
    unzip ATM6-1.8.26-server.zip -d atm6

RUN mkdir -p /atm6/mods
RUN mkdir -p /atm6/world
COPY ./mods/spark-1.9.1-forge.jar /atm6/mods/spark-1.9.1-forge.jar
COPY ./world/ /atm6/world/
COPY ./server.properties /atm6/server.properties
COPY ./eula.txt /atm6/eula.txt
RUN chmod 755 /atm6/startserver.sh