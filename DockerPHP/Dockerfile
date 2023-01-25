# Escojemos la versión php que queramos
FROM php:7.4-cli
# Copiamos nuestra aplicación de nuestra máquina virtual al fichero deseado dentro del docker 
COPY ./api.php /tmp
# seleccionamos el directorio de trabajo
WORKDIR /tmp
# Ejecutamos la aplicación
CMD ["php","./api.php"]
