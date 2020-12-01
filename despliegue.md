## Despliegue de un contenedor httpd con una paǵina personalizada y mapeada por el puerto 8082.

### Añadimos un contenedor.
- Usaremos una plantilla, en nuestro caso buscamos httpd.

![httpd](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd.JPG)

- Creamos el contenedor.

![httpd2](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd2.JPG)

- Ponemos el puerto 8082 en configuraciones avanzadas.

![httpd3](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd3.JPG)

### Comprobar contenedores y configurar.

- Ir a la pestaña containers/contenedores del panel de control.

![httpd4](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd4.JPG)

- Entrar en el que hemos creado previamente e iniciar la consola.

![httpd5](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd5.JPG)
![httpd6](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd6.JPG)


- Añadir una plantilla.
    - Busca una plantilla para tu web aquí (gratuitas) : [enlace](https://freewebsitetemplates.com/)

- Posicionarnos en la carpeta htdocs e insertamos la plantilla descargada.

![httpd7](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/httpd7.JPG)

- Modificamos a nuestro gusto la web.
    - Poner en el navegador *localhost:8082* y listo.
    
![web](https://github.com/estebancr1993/docker-portainer/blob/main/imagenes/despliegue/web.JPG)


---

[ATRAS](https://github.com/estebancr1993/docker-portainer)
