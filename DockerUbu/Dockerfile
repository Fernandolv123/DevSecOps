#Descargamos la única versión de ubuntu
FROM ubuntu:latest
# actualizamos y descargamos apache
RUN apt update
RUN apt install -y apache2
RUN apt install -y apache2-utils
#Cambiamos variables de entorno
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_RUN_DIR /var/www/html
#RUN systemctl start apache2
RUN DEBIAN_FRONTEND=noninteractive apt install -y tzdata
RUN apt-get install php8.1 -y
RUN apt-get install git -y
WORKDIR /var/www/html/
# clonamos la aplicacion de calculadora
RUN git clone https://gist.github.com/9a87a1c43bd923eb939a.git
#Exponemos el puerto 80
EXPOSE 80
#Activamos apache
ENTRYPOINT ["/usr/sbin/apache2"]
CMD ["-D", "FOREGROUND"]
