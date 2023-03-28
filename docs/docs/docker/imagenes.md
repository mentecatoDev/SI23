# Imágenes
Una imagen de Docker es un paquete de software que contiene todo lo necesario para ejecutar una aplicación, incluyendo el código, las dependencias, el sistema operativo, las bibliotecas y las configuraciones. 
Las imágenes de Docker se utilizan como **plantillas** para crear **contenedores** de Docker, que son instancias en tiempo de ejecución de una imagen. Las imágenes se crean a partir de un archivo de configuración llamado `dockerfile`, que especifica los componentes y configuraciones necesarios para la aplicación.
Una vez que se ha creado una imagen de Docker, se puede almacenar en un registro de imágenes de Docker, como [Docker Hub](docker_hub.md) o un registro privado, para que otros usuarios puedan descargarla y utilizarla en la creación de contenedores.
Las imágenes de Docker son portables y se pueden ejecutar en cualquier sistema que admita la plataforma Docker. Además, como las imágenes están aisladas del sistema operativo del host, se pueden ejecutar varias instancias de la misma imagen en diferentes contenedores sin interferir entre sí.

## ![capas](capas.md)