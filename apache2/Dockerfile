FROM ubuntu:18.04
MAINTAINER kogoon@example.com
LABEL "name"="webserver"
ENV aloha=date
ENV path=/var/www/html
RUN sed -i 's/archive.ubuntu.com/ftp.daumkakao.com/g' /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y apache2
COPY nihao /var/www/html/nihao
COPY hello.html $PATH
ADD aws.tar /var/www/html
WORKDIR /var/www/html
RUN echo ohayo >> ohayo.html
VOLUME /var/www/html          #-v /tmp:/var/www/html
EXPOSE 80
ENTRYPOINT ["apachectl"] # ["apachectl", "-D", "FOREGROUND"] fix possible
CMD ["-D", "FOREGROUND"] # ["apachectl", "-D", "FOREGROUND"]

