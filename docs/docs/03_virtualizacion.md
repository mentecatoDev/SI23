# Arranque de un Sistema Operativo

Ya hemos visto anteriormente que el hardware, por si solo es totalmente incapaz de realizar ninguna acción, necesita un software que le indique que tiene que hacer. Cuando encendemos un sistema informático, estamos poniendo en marcha hardware, por lo que necesitan medios especiales para hacer que se cargue un primer software.


## Arranque Inicial POST


En los ordenadores compatibles actuales el proceso de carga de un sistema operativo cualquiera se compone de una serie de pasos que se inician cuando se enciende o reinicia el ordenador. El proceso comienza siempre en la BIOS, y salvando algunas pequeñas variaciones que puede haber en función de cada fabricante de hardware y del propio BIOS, el desarrollo paso a paso de esta secuencia es el siguiente:

- Cuando se da tensión a la fuente de alimentación y una vez que la alimentación se estabiliza, genera una señal denominada “Power Good” en uno de los cables que va de la fuente de alimentación a la placa base; esta señal es recibida en el  juego de chips instalado en la referida placa, y a su vez genera una señal  de reinicio (**reset**) al **procesador**.

![](SI23/docs/docs/img03/01.png)

- La finalidad de este proceso es evitar que  el  procesador  arranque  prematuramente,  cuando  las  tensiones  de  alimentación no son todavía correctas, lo que podría producir daños en el  hardware. Es el mismo sistema que se utiliza para un reinicio en caliente  cuando pulsa en el botón marcado “Reset”.

![](SI23/docs/docs/img03/02.png)

- El procesador arranca cuando se retira la señal de reset. En este momento  no existe en su memoria ninguna instrucción o dato, por lo que puede hacer absolutamente nada. Para salvar este obstáculo, los fabricantes incluyen en la circuiría (hardware) de la placa base un mecanismo especial. El sistema se dirige a una dirección fija de memoria (la FFFF0h en concreto). Esta dirección, situada muy cerca del final de la memoria del sistema en los primeros ordenadores compatibles, es el punto de inicio de la BIOS. En realidad, este punto de inicio contiene una instrucción de salto (jump) que indica al procesador donde tiene que dirigirse para encontrar el punto donde comienza realmente el programa de carga (**BOOTSTRAP**) de la BIOS. Este programa contenido en esa dirección se lleva a la CPU y se ejecuta.

- La primera parte de este programa de la BIOS inicia un proceso de comprobación del hardware denominado POST (Power On Self Test), en caso de existir errores graves, el programa se detiene emitiendo  una  serie  de  pitidos  [(http://www.bioscentral.com)](http://www.bioscentral.com/)  que  indican  el  tipo  de  error encontrado.  El  orden  de  las  comprobaciones  del  POST  depende  del  fabricante,  pero generalmente la secuencia de comprobaciones se resume como sigue:  
  - Comprobación del procesador  
  - Varias comprobaciones sobre la memoria  
  - Inicializar los dispositivos de video y teclado. La comprobación del dispositivo de video incluye cargar y ejecuta la parte de BIOS incluida en el adaptador de video. La mayoría de las adaptadoras modernas muestran en pantalla información sobre si mismas; es por esta razón por  la  que,  a  veces,  lo  primero  que  se  ve  en  pantalla  es  información  sobre  la  propia controladora de video antes que ningún mensaje de la BIOS del sistema.
  - Determinar el tamaño de la RAM completa y comprobar su funcionamiento (el recuento que se ve en pantalla). Si llegado a este punto existiera algún error en la memoria se mostraría un mensaje de error (el dispositivo de video ya está operativo, así que no hace falta emitir pitidos).

![](SI23/docs/docs/img03/03.png)
  - Inicializar los puertos: COM (comunicaciones serie, LPT (comunicación paralela), USB, S-ATA, SCSI, etc.
  - Inicializar, en su caso, el sistema de disquete.
  - Inicializar el sistema IDE, S-ATAo SCSI. (Discos duros, CDROMS, etc)
  - A continuación, el BIOS recorre la memoria en busca de la posible existencia de otros programas en ROM para ver si alguno tiene BIOS, lo que ocurre, por ejemplo, con los controladores de disco duro IDE/ATA, cuyos BIOS se encuentran en la dirección C8000h; otros elementos que suelen contar con sus propios BIOS son las tarjetas de red y las controladoras SCSI. Estos módulos son cargados y ejecutado.
  - A  continuación,  el  BIOS  muestra  su  pantalla  principal  (generalmente  con  los  créditos  del fabricante  número  de  versión  y  fecha).  Como  hemos  visto,  el  bios  realiza  una  especie  de inventario del sistema y algunas pruebas para verificar que su funcionamiento es correcto, y en esta pantalla muestra un resumen de  los  mismos.  En  los PC  originales  la  configuración  del hardware  disponible  se  efectuaba mediante interruptores (“Jumpers”) situados en la placa-base. Hoy en día se utiliza el estándar PnP (Plug & Play), que es capaz por sí misma de detectar y configurar los dispositivos conectados, asignándoles  los  recursos  necesarios  y  mostrando  un  mensaje  en  pantalla  por  cada  uno instalado.

![](SI23/docs/docs/img03/04.png)


**La última instrucción del programa POST** se encarga de buscar otro programa que pueda ser cargado en  el  procesador  de  PC  para  que  se  encargue  de  seguir  arrancando  el  sistema  informático, normalmente cargando ya un sistema operativo. 

¿Pero dónde buscará el POST el programa a cargar? Y en caso de que existan varios sistemas operativos en varios soportes, ¿cuál de ellos será el elegido?


## Elección y arranque de un sistema operativo

En este punto en el que estamos el programa que está en la CPU es el POST, y ya ha concluido todo su trabajo. Pero si dicho programa simplemente liberará la CPU, el equipo se quedaría colgado ya que ningún otro software entraría en el microprocesador. Por ello, la última misión del POST es buscar otro programa, y cargarlo en la CPU antes de liberarla.   

En  un  sistema  informático  actual  podemos  tener múltiples  discos  duros,  cada  uno  de  ellos  con varias particiones donde pueden estar almacenados varios sistemas operativos, podemos tener un CD en la unidad lectora que también cuente con su propio sistema operativo, podemos tener un disquete de inicio en la disquetera, podemos tener un pequeño sistema operativo en un dispositivo USB, podemos tener un disco duro externo conectado por FireWire; etc. ¿Cómo puede saber el POST a cuál de todos estos programas cederle el control?   

![](SI23/docs/docs/img03/05.png)

![](SI23/docs/docs/img03/06.png)

De momento, en la BIOS de casi todos los equipos modernos es posible encontrar unas opciones que indican cual es el soporte de información desde el cual se va a arrancar el sistema (Boot). 

Normalmente estas opciones se encuentran en la segunda opción que aparece en el menú de la BIOS (opciones avanzadas de la BIOS o Advanced BIOS Features).   

En alguna opción de este menú, normalmente se nos permite indicar varios dispositivos ordenados que utilizaremos para el arranque. Una opción que se puede dejar por defecto es indicar que se arranque desde el Floppy si existe, luego desde el CD, y por fin del HDD, para que nos permita arrancar el sistema desde disquete, si no existe desde CD, y si tampoco hay ningún CD de arranque, desde el disco duro. En las BIOS más modernas, veremos que también podemos indicarle que arranque desde un puerto USB, desde un puerto SATA, etc. 

Si  el  sistema  operativo  se  ![](SI23/docs/docs/img03/07.png)ejecuta desde disquete o CD, no  hay  demasiados  problemas,  dado que en un disquete o en un  CD solo puede haber un único  proceso  de  arranque  para  un  único sistema operativo.    

Sin embargo, es posible que en disco duro tengamos varios sistemas operativos para arrancar en nuestra maquina en varias particiones. Además, podemos tener varios discos duros en nuestro sistema, y en cada disco podemos tener varios sistemas operativos instalados. 

Desde  la  BIOS  vemos  cómo  podemos  indicar  de  qué  dispositivo  queremos  arrancar.  Podemos  indicar normalmente si queremos arrancar desde el disco duro, desde el CD, USB, etc. 

Hay BIOS desde donde se puede indicar incluso desde cuál de los discos duros queremos arrancar (HDD-0, HDD-1, etc.) Hay que tener en cuenta que en algunas BIOS esta facilidad para distinguir entre los distintos discos  duros  no  está  presente,  o  no  funciona  bien.  En  los  casos  en  que  esto  ocurra,  tendremos  que introducirnos en la BIOS y desactivar los discos duros de los que no queremos que arranque. Así, por ejemplo, en un sistema informático de dos discos duros si queremos arrancar desde el primer disco duro no tenemos que hacer nada, pero si queremos arrancar desde el segundo disco duro desactivaremos el primero en la BIOS.   

![](SI23/docs/docs/img03/08.png)

Para desactivar los discos duros, hay que entrar en la primera opción de la BIOS y poner None, not instaled, o algo parecido en el tipo de disco duro que queremos desactivar. Esto no quiere decir que dichos discos duros no se usarán durante el funcionamiento normal de la máquina, sino que no se usarán en el proceso de arranque.   Pero con esto conseguimos indicar al sistema informático que disco duro quiero utilizar para el arranque del sistema... pero resulta que en un solo disco duro puedo tener instalado más de un sistema operativo.   

¿Cómo se le indica al sistema que quiero arrancar con Windows XP, o con Linux, o con Beos si todos estos SO están instalados en el mismo disco duro?   

![](SI23/docs/docs/img03/09.png)

Para entender esto tenemos que comprender bien como está organizado un disco duro. 

### Organización lógica del disco duro. 

Vamos a ver cómo se organiza un disco duro a alto nivel. En el módulo Fundamentos de Hardware tema 2 ya hemos visto cómo se organiza a bajo nivel un disco duro y hemos visto como un disco duro se divide en particiones, los conceptos allí explicados nos serán útiles para entender este tema. 

Las  particiones  son  divisiones  lógicas  efectuadas  en  un  disco  duro.  Responden  a  una  necesidad  muy importante en informática: compartir un mismo disco duro para ![](SI23/docs/docs/img03/10.png) varios  sistemas  operativos.  Cada  partición  tiene  la estructura lógica correspondiente a su sistema operativo. Una partición Windows 98 contiene sector de arranque, FAT, directorio raíz y área de datos, una partición de Windows en NTFS tiene su sector de arranque y MFT, etc. Los datos de una partición no se mezclan con los de otra.   

En un disco duro podemos tener hasta 4 particiones como máximo. De las 4, solo una puede estar definida como activa al mismo tiempo. Esta partición activa será la que cargue el sistema operativo cuando iniciamos el sistema informático.   

El primer sector de cada una de estas particiones se conoce como sector de arranque, y en dicho sector (512 bytes) se almacena un programa especial que es el encargado de arrancar el sistema operativo de dicha partición.   

En el primer sector del disco duro no se sitúa un sector de arranque, en su lugar se sitúa una tabla de particiones (Master Boot Record o MBR). Esta tabla de particiones incluye una tabla donde definimos las 4 particiones que pueden estar presentes en nuestro disco duro y su tamaño y un pequeño programa que permite localizar la partición activa, leer su sector de arranque y usarlo para arrancar nuestro sistema informático.   

Este **MBR** (Master Boot Record) está situado en el primer sector del disco duro, de modo que su tamaño es de 512 bytes. En esta capacidad se almacena lo siguiente por cada MBR:   



| direccion                               | contenido                             | tipo      |
| --------------------------------------- | ------------------------------------- | --------- |
| +000h                                   | Programa MBR                          | 445 Bytes |
| +1BEh                                   | 1º entrada de la tabla de particiones | 16 Bytes  |
| +1CEh                                   | 2º entrada de la tabla de particiones | 16 Bytes  |
| +1DEh                                   | 3º entrada de la tabla de particiones | 16 Bytes  |
| +1EEh                                   | 4º entrada de la tabla de particiones | 16 Bytes  |
| +1FEh                                   | Identificación (AA55h)                | 2 Bytes   |
| Contenido del Master Boot Record o MBR. |                                       |           |

Longitud = 200h = 512 Bytes. 

El código AA55h marca este sector como ejecutable.  

Vemos como existe un programa al principio conocido como programa MBR que ocupa 445 Bytes.   

Un programa MBR estándar leerá la tabla de particiones y escogerá de cuál de esas particiones va a arrancar el sistema operativo. No lo hará como podría parecer lógico de la primera partición, sino de la partición primaria que está marcada como activa. El MBR lee el primer sector de esa partición, y le cede el control de la CPU a ese programa (Boot Sector o Sector de Arranque).   

Hay que indicar que no existe un programa MBR estándar. En realidad, el código que se encuentra aquí puede ser muy variado, aunque normalmente todos son compatibles. Podemos instalar programas MBR conocidos como gestores de arranque que amplían las posibilidades el gestor de arranque MBR instalado por defecto.   

Hay que prestar atención a lo que se ha dicho. Si se arranca desde un disco duro, se lee el primer sector (MBR) y este a su vez, lee un segundo sector (Boot Sector). Vemos también como existen 4 entradas para almacenar hasta 4 particiones, de aquí viene el límite de 4 particiones para un disco duro.  También vemos como por cada partición se almacena su tipo con 16 bytes. En estos 16 bytes se almacena lo siguiente:   


| Dirección | Contenido                                                    | tipo   |
| --------- | ------------------------------------------------------------ | ------ |
| +00h      | Estado de la partición: 00h – Inactiva  80h arranque (activa) | 1 Byte |
| +01h      | Cabeza de lectura / escritura donde comienza la partición.   | 1 Byte |


| +02h                                                         | Sector y cilindro donde comienza la partición.               | 2 Byte  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------- |
| +04h                                                         | <p>Tipo de partición: </p><p>00h – Libre   </p><p>01h – DOS con la vieja FAT de 12 bits. 02h – XENIX </p><p>03h – XENIX </p><p>04h – DOS con FAT 16   </p><p>05h – Partición extendida. </p><p>06h – Partición DOS > 32 Megas. 0Bh – Windows FAT32 0Ch – Windows FAT 32 LBA 0Eh – VFAT </p><p>16h – Hidden FAT 16 (Oculta) 63h – Unix </p><p>65h – Novell Netware </p><p>Etc..... </p> | 1 Byte  |
| +05h                                                         | Cabeza de lectura / escritura donde termina la partición.    | 1 Byte  |
| +06h                                                         | Sector y cilindro donde termina la partición.                | 2 Bytes |
| +08h                                                         | Dirección del primer sector de la partición. (Sector de arranque). | 4 Bytes |
| +0Ch                                                         | Número de sectores en esta partición.                        | 4 Bytes |
| Contenido de cada una de las 4 entradas de la tabla de particiones. Longitud = 10h = 16 Bytes. |                                                              |         |

Vemos como el 1º campo se usa para indicar si esta partición es la activa o no. El 2º y 3º campo se usa para indicar el cilindro, sector y cabeza donde comienza la partición.   

El 4º campo se usa para almacenar el tipo de la partición, aquí se indica que sistema operativo está instalado en la partición, si dicha partición esta oculta o no, etc.  El 5º y 6º campo se usa para indicar el cilindro, sector y cabeza donde termina la partición.   

El 7º campo indica la dirección del primer sector de la partición (el sector de arranque) para que el POST pueda pasarle el control. Este sector siempre es el 1o sector de la partición, pero aquí indicamos su valor director (no de sector) y no la combinación cilindro, sector y cabeza. Esto se hace para que el acceso al sector de arranque sea más rápido, y para evitar posibles errores en la carga del sistema.   

El 8º campo se usa para almacenar el número total de sectores que existen en la partición. Es un campo que se usa para comprobar que los datos de la partición son correctos.  

Las particiones de un disco duro pueden ser de dos tipos:   

- Primarias 
- Extendidas   

Como ya vimos anteriormente, en un disco duro puede existir un máximo de 4 particiones, sin embargo, sólo una de estas particiones puede ser extendida. (Si seguimos las recomendaciones del estándar usado para organizar lógicamente los discos duros).   

Cada partición **primaria** forma su propio volumen de datos (la letra en Windows, para entendernos) y tiene su propio sector de arranque. Son las particiones normales.   

Una partición **extendida**, sin embargo, no forma ningún volumen, ni tiene un sector de arranque como tal. Una partición extendida en realidad es un contenedor de unidades lógicas. Se pueden crear tantas unidades lógicas  en  una  partición  extendida  como  se  deseen.  A  términos  prácticos,  estas  unidades  lógicas  se comportan como particiones primarias.   

Cada unidad lógica que se crea dentro de una unidad extendida forma su propio volumen, aunque no tiene un sector de arranque real, sino que usa su sector de arranque para controlar su tamaño entre otras cosas.   

De esta manera, si dividimos un disco duro en una partición primaria (un volumen) y una partición extendida (donde creamos 10 unidades lógicas, cada una con su propio volumen) formaremos un total de 11 volúmenes (11 letras de unidad) pero solo tendremos un sector de arranque usable como tal, el de la partición primaria. 

Solo el sector de arranque de una partición primaria es válido para arrancar el sistema operativo. El sector de  arranque  de  la  partición  extendida  solo  contiene  información  sobre  las  unidades  lógicas  que  se encuentran dentro de ella (tamaños, comienzos y finales, etc.). 

La tabla del MBR identifica la localización y tamaño de la partición extendida, pero no contiene información sobre las unidades lógicas creadas dentro de esta partición extendida. Ninguna de estas unidades lógicas puede ser marcadas como activas, por lo que es posible que instalemos un sistema operativo en alguna de estas particiones lógicas, pero nunca podrá ser cargado **directamente**, ya que no podemos marcar esa partición como activa, y por lo tanto no podemos indicar que sea el volumen de arranque. (Para poder instalar sistemas operativos en estas unidades lógicas, tendremos que usar un programa conocido como gestor de arranque que veremos posteriormente, estos gestores de arranque suelen guardar los programas usados para cargar los sistemas operativos siempre en la partición activa del disco duro).   

Hemos visto como el MBR se divide en dos partes bien diferenciadas, el programa MBR que ocupa la mayor parte del MBR y la tabla de particiones vista anteriormente.   

#### GPT   

Hemos visto en el punto anterior como funciona un disco duro con una tabla de particiones MBR, que es la opción  más  habitual  con  la  que  nos  vamos  a  encontrar.  Sin  embargo,  desde  hace  un  tiempo  se  está substituyendo nuestras antiguas BIOS por un sistema más moderno conocido como EFI (Extensive Firmware Interface).   

Este sistema, totalmente incompatible con BIOS, permite que en el disco duro nos olvidemos si queremos de la MBR y utilicemos un sistema mucho más potente, conocido como GPT (GUID Partition Table, siendo GUID acrónimo de Globally Unique Identifiers).   

GPT usa un moderno modo de direccionamiento lógico (LBA, logical block addressing) en lugar del modelo cilindro-cabeza-sector (CHS) usado con el MBR. La información de MBR heredado está almacenada en el LBA 0 o bloque lógico 0, la cabecera GPT está en el LBA 1, y la tabla de particiones en sí en los bloques sucesivos. En los sistemas operativos Windows de 64-bits, 16.384 bytes, o lo que es lo mismo, 32 sectores, están reservados para la GPT, dejando el bloque LBA 34 como el primer sector usable del disco.   

GPT proporciona asimismo redundancia. La cabecera GPT y la tabla de particiones están escritas tanto al principio como al final del disco.   

![](SI23/docs/docs/img03/11.png)

Vemos como al principio del disco se guarda un sector conocido como protective MBR. El propósito de este sector es permitir que programas y sistemas que están preparados solo para trabajar con MBR y no con GPT puedan ver el disco como válido.   

Este MBR “falso” está configurado con una sola partición que ocupa todo el disco, y es totalmente obviado por EFI, por lo que no se utiliza nunca. Sin embargo, si un programa o sistema operativo antiguo intenta usar este disco, creerá que el disco duro es un MBR normal de 1 sola partición, y cuando intente acceder al disco duro, se dará cuenta que la información almacenada en el no coincide con lo que él espera, y mostrará un mensaje indicando que la estructura del disco duro esta corrompida, que no encuentra el sistema, o algo parecido.   

Es este el gran fallo de GPT, que solo es compatible con los nuevos sistemas operativos y los nuevos programas. Por poner un ejemplo, si instalamos Windows 7 64 bits configurando el disco como GPT, si luego queremos instalar un sistema operativo anterior en ese mismo disco duro, el propio sistema nos indicará en la instalación que no puede trabajar con el disco duro ya que esta corrompido, y no podremos instalar el sistema.   

Por ejemplo, todas las versiones de Windows 7 pueden leer discos GPT, pero solo las versiones de 64 bits de Windows 7 pueden arrancar desde un disco duro GPT.   

La cabecera de la tabla de particiones (Primary GPT Header) define los bloques de disco que pueden ser utilizados por el usuario (bloques usables). También define el número y tamaño de las entradas de partición que conforman la tabla de particiones. En Windows hay 128 entradas de partición reservadas, cada una de 128 bytes de longitud. Así, se pueden crear hasta 128 particiones si usamos un sistema tipo Windows.   

La cabecera contiene el GUID del disco (Globally Unique Identifier, Identificador Global Único). Registra su propio tamaño y localización (siempre LBA 1), y el tamaño y la localización de la cabecera y tabla de la GPT secundarias (siempre en el último sector del disco). Contiene una suma de comprobación CRC32 para sí mismo y para la tabla de partición, que se verifica por los procesos EFI durante el arranque. Además, todo GPT está configurado para usar Unicode.   

Para entender mejor por qué se crea GPT, veamos los principales problemas que presentan MBR y las ventajas que aporta GPT.   

### Problemas con el MBR 

1. En MBR sólo pueden ser definidas 4 particiones primarias o 3 primarias + 1 partición extendida (con un número arbitrario de particiones lógicas dentro de la partición extendida).  
1. En MBR dentro de la partición extendida, los metadatos de las particiones lógicas se almacenan en una estructura de lista enlazada. Si un enlace se pierde, todas las particiones lógicas existentes, después de los metadatos, se pierden.  
1. MBR sólo admite 1 byte para códigos de tipo de partición, lo que conlleva muchas colisiones.  
1. MBR almacena la información del sector de la partición con valores LBA de 32 bits. Esta longitud de LBA junto con los 512 byte del tamaño del sector (más comúnmente utilizados) limita el tamaño máximo manejable del disco hasta 2  

### Ventajas de GPT

1. Utiliza GUID (UUID) para identificar los tipos de particiones. Sin colisiones.  
1. Proporciona un GUID único de disco y un GUID único de partición para cada partición. Un buen sistema de archivos independiente referenciando a las particiones y discos.   
1. Número arbitrario de particiones (depende del espacio asignado por la tabla de particiones). No hay necesidad de particiones extendidas y lógicas. Por defecto, la tabla GPT contiene espacio para la definición de 128 particiones. Sin embargo, si el usuario desea definir más particiones, se puede asignar más espacio (de momento solo en Linux).   
1. Utiliza 64-bit LBA para almacenar números del Sector - tamaño máximo del disco manejable es de 2 Zeta Bytes.   
1. Almacena una copia de seguridad del encabezado y de la tabla de particiones al final del disco que ayuda en la recuperación en el caso de que los primeros están dañados.   
1. Código de reparación de errores CRC32 para detectar errores y daños de la cabecera y en la tabla de particiones. 

## Comandos para comprobar particiones del disco y administrador de discos de Windows
### Diskpart 
En esta ocasión vamos a estudiar los comandos básicos para ver las particiones creadas en los discos duros de nuestro equipo, tanto internos como unidades extraíbles.
Para conocer estos comandos, se adjunta un enlace a una página web con la explicación sobre la herramienta  “diskpart”, disponible en Windows:

[Acceder a guía de uso de diskpart desde el cmd](https://www.profesionalreview.com/2019/01/18/utilizar-diskpart/)

>Es muy importante que abráis la ventana de comandos (cmd) como administrador.

Si quieres ver el uso de esta herramienta, puedes también ver el siguiente vídeo tutorial que elaboró el  profesor Jose Antonio pasado:

[Vídeo del uso de diskpart en Windows](https://www.youtube.com/watch?v=cEGdxsAazBM)  

Os aconsejo que intentéis los comandos mientras veis el vídeo, ya que en breve será tu turno.  

### Administrador de discos

Existe una herramienta alternativa gráfica, que nos proporciona Windows 7 y versiones posteriores que se llama administrador de discos.
![](SI23/docs/docs/img03/12.jpeg)
Con esta herramienta podemos ver, de forma gráfica, toda la información de los diferentes discos duros del equipo.  

Para acceder a esta herramienta tenemos varias opciones:  
- Botón derecho sobre el icono de Inicio, seleccionamos “Administración de discos” en el menú emergente.  
- Escribir “administración de discos” en el buscador de Windows y pulsamos en la opción encontrada.
- Pulsar en el teclado la combinación de teclas `Windows + R`. En el menú ejecutar escribimos `diskmgmt.msc`.

## Arranque de Windows 

### Arranque de Windows 7/Vista/2008/8/10  

La secuencia de arranque de Windows cambió a partir de XP. La principal diferencia estriba en que se ha cambiado el gestor de arranque, ya no se usa el `ntldr`, sino que se usa el Windows Boot Manager (`bootmgr`).   

Mientras que el gestor `ntldr` usaba un fichero de texto denominado `boot.ini` para configurar sus opciones, `bootmgr` utiliza una base de datos conocida como Boot Configuration Data (BCD) que no puede ser editada directamente como lo era el `boot.ini` ya que no es un fichero de texto.   

El BCD es una base de datos con datos sobre la configuración del arranque que se suele almacenar en \\Boot\\Bcd.   

1. Se carga y ejecuta el **POST**
1. Se carga el **MBR** del disco duro (si es la opción elegida en la BIOS)  
1. Se carga el **sector de arranque** de la partición primaria activa   
1. Se carga el programa `bootmgr`   
1. `bootmgr` ajusta el procesador para trabajar a 32 bits o 64 bits.   
1. `bootmgr` lee la base de datos **BCD** y muestra un menú si es necesario   
1. El usuario selecciona un sistema operativo del menú, o se carga por defecto uno de ellos 
1. `bootmgr` carga `winload.exe`
1. `winload.exe` carga `NTOSKRNL.EXE` (Núcleo del sistema operativo o Kernel).
1. `NTOSKRNL.EXE` lee el **registro** de Windows, y procede a ir cargando el sistema completo.  

Windows dispone de un comando para configurar esta base de datos BCD, el `bcedit.exe`, pero es realmente engorroso de usar. Es mejor usar una utilidad grafica de una 3rd party (tercera compañía, una compañía distinta a la que realiza el sistema) como puede ser `EasyBCD` que permite configurar muchas más opciones que el `bcedit.exe` y de forma mucho más fácil.

#### Novedades en Windows 8 / 10

Aunque el arranque de Windows actual es muy similar al de Windows 7 incorpora varias novedades, muchas de ellas basadas en el uso de UEFI en lugar de BIOS. Una de las más importantes es la del Secure Boot. 

#### SECURE BOOT

Los ordenadores cuando encontraban el sector de arranque del SO que querían cargar, se limitaban a ejecutar dicho código, sin comprobar de ningún modo qué es lo que se está ejecutando.   

Sin embargo, si contamos en el sistema con UEFI en lugar de BIOS y esta activada una característica conocida como  **Secure  Boot**,  el  firmware  del  sistema  comprueba  la  firma  digital  del  sector  de  arranque,  para comprobar si es de un sistema reconocido, y si se ha producido algún tipo de modificación sobre el mismo. Para permitir el arranque del sistema operativo, se deben dar una de las siguientes situaciones:   

- El código de carga fue firmado utilizando un certificado “de confianza”. Por ejemplo, un certificado de Microsoft. 
- El usuario ha aprobado la firma digital del código de carga. UEFI debería permitir al usuario realizar esta acción. (No siempre ocurre).  
- El usuario deshabilita Secure Boot en la configuración de UEFI.  
- El usuario deshabilita totalmente UEFI, y en su lugar utiliza BIOS.  

#### TRUSTED BOOT

Una vez que secure boot ha terminado su cometido, el código de carga (bootloader) verifica el firmado del kernel de Windows 8 antes de cargarlo. A su vez, el kernel de W8 verifica todos los componentes de Windows que se van cargando, incluyendo los drivers de dispositivo de la propia Microsoft que se cargan en el arranque. Si un fichero ha sido modificado, el bootloader detecta el problema y se niega a seguir cargando el componente. Windows 8 intenta reparar el componente corrupto automáticamente.  

#### FAST STARTUP  

Windows Fast Startup (Inicio rápido) es la opción por defecto a utilizar en Windows 8, Windows Server 2016 y Windows 10 siempre que se utilice UEFI.  

En un sistema Windows en cada momento se encuentran ejecutándose dos sesiones en realidad, la del usuario actual y la del kernel del sistema. Cuando en Windows 7 se apaga el sistema, se cierran ambas sesiones y hay que volver a cargarlas desde cero cuando el sistema se inicia. 


## Arranque de sistemas Linux  

Este proceso de arranque comienza desde que el **MBR o GPT**, busca el sector de arranque de la partición en la que se encuentra el sistema operativo de Linux.   

En las actuales distribuciones de Linux, cuando accedamos al sector de arranque nos encontraremos con un **gestor de arranque** llamado **GRUB** (Grand Unified Bootloader). Grub es un gestor de arranque múltiple, desarrollado bajo licencia GNU, que nos permite elegir el sistema operativo del que queremos arrancar. GRUB, no suele tener problemas de compatibilidad para permitir el arranque de cualquier sistema operativo, como los OS o Windows entre otros.  

En este caso nos vamos a centrar en el arranque de un Sistema Linux basado en Debian, como Ubuntu. Partimos con la carga de GRUB del sector de arranque y seleccionando el Sistema Linux.  

En este momento se entra en la **fase del Kernel** de Linux, que es cargado como un archivo comprimido de imagen de tipo zlib). Entonces se cargan los elementos hardware mínimos para poder continuar con su carga.   

Mediante la función **startup** del kernel, este se descomprime y se carga completamente en memoria, detecta el tipo de procesador y carga muchas funciones de inicialización.  

En la siguiente etapa, se ejecuta el **proceso init** cuya función es conseguir que todo el sistema se cargue por completo. Se encarga del montaje del sistema de archivos, inicia los servicios de usuario necesarios y cambia al entorno de usuario cuando el proceso ha finalizado.   

Ya estaríamos ante la Shell para introducir nuestras credenciales.

## Modos de Red en VirtualBox



| Modo red | Dirección red | Guest-Host | Host-Guest | MM.VV. | Red local-Host | Internet | Descripción                                                  |
| - | - | - | - | - | - | - | - |
| NAT | 10.0.X.0/24 (X=2,3,4,5)| Sí| No| No| No| Sí| Cada invitado tiene su dirección propia y navega de forma aislada. Se comunica con el anfitrión y con Internet mediante un router NAT virtual. |
| Adaptador puente| Red anfitrión| Sí         | Sí         | Sí     | Sí             | Sí| El invitado usa la tarjeta de red del anfitrión usando un puente(Bridge). |
| Red NAT                                                      | Red virtual configurada     | Sí         | No         | Sí     | No             | Sí       | Red virtual NAT en la que las MMVV de la misma red virtual pueden comunicarse.Tiene comunicación al exterior con NAT.</p> |
| Red interna                                                  | Configurar manualmente      | No         | No         | Sí     | No             | No       | Las máquinas virtuales forman una red interna entre ellas sin comunicación al exterior. Deben configurarse las tarjetas de red manualmente. |
| Sólo- anfitrión                                              | Red desde Adaptador virtual | Sí         | No         | Sí     | No             | No       | Es similar a la red interna pero permiten la comunicación con el anfitrión para aprovechar sus servicios. Funciona aunque no haya cable de red conectado. |

Estas configuraciones son las mostradas en el caso en el que cada máquina virtual monte una única tarjeta de red, sin que haya otras tarjetas de red que puedan hacer de adaptador puente con otras redes. 