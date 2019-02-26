FROM ubuntu:16.04
MAINTAINER praveenreddy
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y  software-properties-common && add-apt-repository ppa:webupd8team/java -y
RUN apt-get update
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install -y oracle-java7-installer && apt-get clean
COPY https://s3-us-west-2.amazonaws.com/gameoflifewar/spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar /gol.jar
EXPOSE 9010
CMD java -jar gol.jar

