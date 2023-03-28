# Introducción
La configuración adecuada de un entorno de desarrollo local sigue siendo un gran reto a pesar de todos los otros avances de la programación moderna. Simplemente hay demasiadas variables: diferentes ordenadores, sistemas operativos, versiones de lenguajes y frameworks, opciones de entornos virtuales,  y así sucesivamente. Cuando se añade el reto de trabajar en equipo en un entorno en el que todos necesitan tener la misma configuración, el problema se magnifica.

En los últimos años ha surgido una solución: [Docker](https://www.docker.com/). Aunque sólo tiene unos pocos años, Docker se ha convertido rápidamente en la opción por defecto para muchos desarrolladores que trabajan en proyectos a nivel de producción.

Con Docker finalmente es posible reproducir un entorno de producción de forma fiel y fiable localmente, desde la versión adecuada de Python hasta la instalación de Django a la par de ejecutar servicios adicionales como una base de datos a nivel de producción. Esto significa que ya no es importante si se desarrolla en un equipo Linux, Mac o Windows. Todo funciona dentro del mismo Docker.

Docker también facilita exponencialmente la colaboración en equipo. Atrás quedaron los días de compartir archivos README largos y obsoletos para añadir un nuevo desarrollador a un proyecto de grupo.

En lugar de eso, con Docker sólo se tienen que compartir dos archivos: `Dockerfile` y  `docker-compose.yml` y el desarrollador puede tener la confianza de que su entorno de desarrollo local es exactamente igual que el del resto del equipo.

Docker no es una tecnología perfecta. Todavía es relativamente nueva y compleja bajo el capó; aún está en desarrollo activo. Pero aspira a la promesa de una política coherente y a un entorno de desarrollo compartible, que pueda ejecutarse localmente en cualquier ordenador o desplegado en cualquier servidor, lo que lo convierte en una opción sólida.

## ¿Qué es Docker?
Docker es una forma de aislar todo un sistema operativo a través de **contenedores Linux** que son un tipo de virtualización. La virtualización tiene sus raíces en los inicios de la informática cuando las computadoras grandes y caras eran la norma. ¿Cómo podrían varios programadores utilizar la misma máquina?. La respuesta fue la virtualización y específicamente las máquinas virtuales que son copias completas de un sistema informático desde el sistema operativo en adelante.![https://diveintodocker.com/assets/courses/virtual-machine-vs-docker-container-diveintodocker-da32029afb09e889fdee17b66876493d3b2441f30e77708520cd9bf338a21866.jpg](img00.png)

Cuando se alquila un espacio en un proveedor de cloud computing como Amazon Web Services (AWS) normalmente no se proporciona una pieza de hardware dedicada. En lugar de eso, se comparte un servidor físico con otros clientes. Pero como cada cliente tiene su propio sistema virtual que se ejecuta en el servidor, le parece que tiene el suyo propio.

Esta tecnología es la que hace posible añadir o eliminar servidores de un *servicio de cloud* de forma rápida y sencilla. Se trata en gran medida de software entre bastidores, no de hardware real.

¿Cuál es el inconveniente de una máquina virtual? Tamaño y velocidad. Un sistema operativo huésped típico (*guest*) puede ocupar fácilmente hasta 700MB de tamaño. Así que si un servidor físico soporta tres máquinas virtuales, eso es al menos 2,1 GB de espacio en disco ocupado junto con el resto de necesidades para otros recursos como CPU y memoria.

Al entrar en Docker, la idea clave es que la mayoría de los ordenadores dependen del mismo sistema operativo [Linux](https://es.wikipedia.org/wiki/GNU/Linux). ¿Y si virtualizamos desde la capa de Linux hacia arriba? ¿No proporcionaría eso una forma más rápida y ligera de duplicar gran parte de la misma funcionalidad? La respuesta es sí. Y en los últimos años los contenedores [Linux](https://en.wikipedia.org/wiki/List_of_Linux_containers) se han vuelto muy populares. Para la mayoría de las aplicaciones -especialmente las aplicaciones web- una máquina virtual proporciona mucho más recursos de los que se necesitan y un contenedor es más que suficiente.

Esto, fundamentalmente, es Docker: ¡una forma de implementar contenedores Linux!

Una analogía que podemos usar es la de los edificios y los apartamentos. Las máquinas virtuales son como viviendas: edificios independientes con su propia infraestructura, incluida la fontanería y calefacción, así como cocina, baños, dormitorios, etc. Los contenedores Docker son como los apartamentos: comparten una infraestructura común como la fontanería y la calefacción, pero vienen en varios tamaños que se ajustan a las necesidades exactas de un propietario.

## Contenedores vs. Entornos Virtuales

Como programador de Python, por ejemplo, se debe estar familiarizado con el concepto de **entornos virtuales** que son una forma de aislar los paquetes Python. Gracias al entorno virtual, una computadora puede ejecutar múltiples proyectos localmente. Por ejemplo, el Proyecto A podría usar Python 3.4 y Django 1.11 entre otras dependencias; mientras que el Proyecto B usa Python 3.8 y Django 2.2. Configurando un entorno virtual dedicado en cada proyecto se puede gestionar estos diferentes paquetes de software sin contaminar nuestro entorno global.

Hay una pequeña confusión derivada de que hay múltiples herramientas en este momento para implementar un entorno virtual: desde `virtualenv`, `venv` a `pipenv` o `poetry`, pero fundamentalmente todas hacen lo mismo.

La mayor distinción entre los entornos virtuales y Docker es que los entornos virtuales sólo pueden aislar paquetes Python. **No pueden aislar a los no-Python como una base de datos** PostgreSQL o MySQL. Y siguen dependiendo del sistema global; de la instalación de Python a nivel de sistema (en otras palabras, de **su** ordenador). **Los entornos virtuales apuntan a una instalación Python existente; no contienen Python en sí mismos**.

Los contenedores Linux van un paso más allá y **aíslan todo el sistema operativo**, no sólo las partes de Python. En otras palabras, instalaremos el propio Python dentro de Docker, así como se instalará y ejecutará en él la base de datos a nivel de producción.

