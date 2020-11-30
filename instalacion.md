## Proceso de instalación de Portainer en linux

Portainer se compone de dos elementos, **Portainer Server** y **Portainer Agent**. Ambos elementos se ejecutan como contenedores Docker ligeros en un motor Docker o dentro de un clúster Swarm. Debido a la naturaleza de Docker, *existen muchos escenarios de implementación posibles*, sin embargo, a continuación utilizaremos el escenario de configuración en linux.

**ATENCIÓN:** Portainer solo es oficialmente compatible con ***Linux*** (CentOS 7 y 8, Ubuntu 16.04.6 LTS, 18.04.4 LTS y 20.04 LTS) y ***Windows*** (Win 10> 1909 y Server 2019> 1909). Portainer no se prueba en MacOS ni en ningún otro sistema operativo. 


### Implementar Portainer Server en un host LINUX Docker independiente

Utilice los siguientes comandos de Docker para implementar Portainer Server; tenga en cuenta que el agente no es necesario en hosts independientes, sin embargo, proporciona una funcionalidad adicional si se utiliza (consulte el escenario de portainer y agente a continuación): 

>$ docker volume create portainer_data

>$ docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce

***Solo necesitará acceder al puerto 9000 del motor Docker donde se ejecuta portainer usando su navegador, con la dirección http://localhost:9000***

***Nota:*** *El puerto 9000 es el puerto general utilizado por Portainer para el acceso a la interfaz de usuario. El puerto 8000 es utilizado exclusivamente por el agente EDGE para la función de túnel inverso. Si no planea utilizar el agente de borde, no necesita exponer el puerto 8000*

***Nota 2:*** *la opción* ***-v /var/run/docker.sock:/var/run/docker.sock*** *solo se puede utilizar en entornos Linux.*

