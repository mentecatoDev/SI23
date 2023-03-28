# Capas

Las imágenes se construyen sobre una tecnología de **sistema de ficheros por capas**.
Para crear una imagen, generalmente se crea el archivo de texto `dockerfile` formado por diferentes **instrucciones**. Cada línea representa una instrucción, y cada vez que se ejecuta el dockerfile se ejecutan dichas instrucciones de arriba a abajo.
Estos `dockerfile`-s se almacenan como texto y se pueden compartir con facilidad, así como almacenarse en sistemas de control de versiones.
Cada **instrucción** que se ejecuta cambia ligeramente el estado del sistema de archivos respecto a la instrucción anterior.
La diferencia entre el estado del sistema de ficheros antes y después de cada instrucción se guarda en disco como un archivo, que conforma una **capa**.
Cada **imagen** es un conjunto de capas que contienen los diferentes cambios que se van realizando sobre el sistema de archivos empaquetados.
Al final del `dockerfile`, la última instrucción define el **comando** que se ejecutará cuando arranquemos el contenedor.
Al ejecutar un comando a partir de la imagen creada, se ejecuta el comando especificado y se convierte en el proceso con PID 1 dentro del árbol virtual de procesos.
El contenedor seguirá en marcha mientras el proceso creado siga en ejecución.