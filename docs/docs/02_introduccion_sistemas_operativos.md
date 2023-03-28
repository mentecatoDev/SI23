# Introducción a los Sistemas Operativos

## Software 

Tal  y  como  se  define en  el  Diccionario  de  la  lengua  española,  de  la  Real Academia (DRAE), el software es el  **«conjunto de programas, instrucciones y reglas informáticas para ejecutar ciertas tareas en una computadora»**.  

Según  el  estándar  729  del  IEEE,  el  software  es  **«el  conjunto  de  los  programas  de cómputo, procedimientos, reglas, documentación y datos asociados que forman parte de  las  operaciones  de  un  sistema  de  computación»**,  lo  que  concreta  la  definición anterior.  

Así  pues,  podemos  afirmar  que  el  software  es  la  parte  lógica  de  un  ordenador,  a diferencia de la parte física, a la que denominamos hardware. 

## Software Propietario y Software Libre

Es importante dejar clara la diferencia que existe entre el software libre y el software propietario.  

El  **software libre** permite a los  **usuarios** que lo adquieren  **trabajar con toda la libertad sobre él, pudiendo usarlo, copiarlo, estudiarlo, modificarlo y distribuirlo de nuevo una vez  modificado**,  y  así  lo  indica  la  Fundación  para  el Software Libre (Free Software Foundation).  

Esto no implica expresamente que el software sea gratuito, sino que lo es el uso que se le puede dar una vez adquirido, bien sea previo pago, o bien gratuitamente. 

Lo  contrario  es  el  software  propietario,  cuyas  limitaciones  para  el  usuario  que  lo adquiere  son  la  de  copia,  modificación  o  distribución;  tanto  modificado  como  no modificado. 

Según la Fundación para el Software Libre, el software propietario es cualquiera que no cumpla todas las condiciones del software libre. 

Precisamente, se denominan  «cuatro libertades» aquellas que cumple por completo el software libre, y son las siguientes: 

- **Libertad 0:** libertad para utilizar el programa con cualquier propósito. 
- **Libertad 1:**  libertad para estudiar el funcionamiento del programa y adaptarlo a las necesidades del usuario. 
- **Libertad 2:** libertad para distribuir copias del programa. 
- **Libertad  3:**  libertad  para  modificar  el  programa,  mejorándolo  y  haciendo  públicas estas mejoras al resto de usuarios, para beneficio de toda la comunidad. 

Obviamente, para poder llevar a cabo las libertades que implican la modificación del programa,  es  necesario  disponer  del  código  fuente,  por  lo  que  éste  se  tiene  que distribuir para que sea considerado software libre. 

Es muy importante no confundir el término software libre (free software) con “freeware” que es un tipo de software que se distribuye sin costo alguno pero que mantiene su licencia  (copyright),  por  lo  que  no  puede  modificarse  o  utilizar  libremente  como  sí puede hacerse con el software libre; en ocasiones se trata de una versión reducida de un programa más completo de pago. El freeware es una variante gratuita del shareware, el cual es un tipo de software de evaluación, el cual tiene una limitación en el tiempo de uso o en algunas de sus funciones para que el usuario pueda probarlo y si le gusta, lo compre habilitando toda su funcionalidad. 

## Clasificación del Software

El  software  podemos  clasificarlo  principalmente  en  los  siguientes  tipos  según  su finalidad: 

### Software de base 

El  software  de  base,  también  denominado  «software  de  sistema»,  **es  aquel  que  nos permite interactuar directamente con el hardware de nuestro equipo,** actuando como mediador entre el software de aplicaciones y el hardware del sistema.  

Dentro  del  software  de  base  podemos  hacer  una  nueva  clasificación,  donde  se encuentran los siguientes tipos de software: 

- **Sistemas Operativos:**  son  una  parte  esencial  en  el  equipo, ya  que  se  encargan  de gestionarlo todo para que su uso resulte sencillo y efectivo para el usuario. 
- **Controladores  de  dispositivo:**  proporcionan  al  sistema  operativo  instrucciones concretas para interactuar con los dispositivos que tiene instalados el equipo. 
- **Herramientas  de  diagnóstico  y  optimización:**  se  encargan  de  recoger  valores  de parámetros  del  sistema  y,  si  procede,  corregirlos  para  garantizar  el  buen funcionamiento de este.

### Software de programación 

Se denomina así al conjunto de aplicaciones mediante las cuales **un programador puede desarrollar sus programas informáticos.** 

Al  igual  que  en  el  caso  anterior,  cuando  hablamos  de  este  tipo  de  software  nos referimos  a  editores  de  texto,  compiladores,  depuradores,  entornos  de  desarrollo integrados (IDE), etc.   

### Software de aplicación 

Se clasifican como software de aplicación aquellos programas que **permiten al usuario realizar tareas específicas en el sistema.**

Este tipo de software incluye las aplicaciones ofimáticas, software dedicado (educativo, médico, empresarial, etc.), aplicaciones de automatización y control industrial, software de diseño gráfico y multimedia, etc.

## Licencias de Software 

### Tipos de licencias genéricas

El software, con independencia del tipo que sea, lleva asociado un tipo de licencia, que establece las condiciones en las que se publica, sus garantías y concesiones. 

Una misma aplicación puede distribuirse con distintas licencias; por ello, estaríamos hablando de aplicaciones diferentes, puesto que la licencia no es la misma. 

La multilicencia se emplea para permitir que una aplicación tenga una vertiente libre, generalmente bajo varias licencias libres, y otra propietaria. 

Por  un  lado,  tenemos  el  software  privativo  con  un  copyright  con  un  conjunto  de restricciones reflejadas en el contrato que se firma entre el licenciante y el usuario del software.  De  forma  general,  este  software  no  puede  usarse  libremente,  no  puede compartirse,  no  puede  accederse  a  su  código  fuente  y  no  puede  estudiarse  ni modificarse. 

Las  licencias  existentes  de  software  libre  son  muchísimas,  podemos  destacar  entre ellas: 

#### **GNU/GPL (GNU is Not Unix/General Public License)**

Este tipo de licencia está representada por Linux, y es la más conocida en el mundo del software libre.  Permite  tanto  la  distribución  de  la  aplicación  como  la de su código fuente. En el caso de que únicamente se distribuyera la aplicación, debe ser posible acceder  a  sus  fuentes  igualmente.  Del mismo modo,  permite  realizar modificaciones, integrando código GPL.

![](SI23/docs/docs/img02/01.png)


El objetivo de este tipo de licencia es asegurar la libertad del código, de modo  que  incluso  las modificaciones realizadas han de ser distribuidas bajo la misma licencia, y no se pueden incluir partes de código patentadas si la patente no  está  liberada.  Además,  suelen  incluir  un  archivo  con  un  historial  en  el  cual  se recogen tanto las modificaciones efectuadas, como los autores involucrados en ellas. 

Una variante es la licencia LGPL (*Lesser GPL*), que permite utilizar  aplicaciones  libres  con  software  propietario,  de modo  que  la  aplicación  es  distribuida  como  si  tuviera licencia  GPL, pero  puede  integrarse  con  otro  tipo  de software prácticamente sin limitaciones. Suele usarse para bibliotecas de programas, más que para programas ejecutables.

![](SI23/docs/docs/img02/02.png)

#### **BSD (*Berkeley Software Distribution*)**

Es una licencia que suele ser usada por los Sistemas BSD, que son sistemas operativos basados en Unix. Esta licencia al contrario que la GPL permite el uso del código fuente en software privativo. 

![](SI23/docs/docs/img02/03.png)

Es una licencia poco restrictiva, ya que permite distribuir la aplicación y el código fuente para ser modificados e integrados con otros programas; sin embargo, y a diferencia de otros tipos, en esta se da crédito a los autores. 

La  utilizan  los  desarrolladores  para  crear  aplicaciones  compatibles  basadas  en  una aplicación ya existente con licencia BSD. 

Como curiosidad, saber que el S.O. macOS está basado en el sistema operativo BSD.

#### **MPL (Mozilla Public License)** 

Esta licencia fue creada por Netscape Communications para su navegador Netscape, y fue la primera con origen en una empresa, con el tiempo el control de esta licencia fue tomado por la Fundación Mozilla.

![](SI23/docs/docs/img02/04.png)

Permite  copiar,  modificar  y distribuir ilimitadamente una aplicación, sin  restringir  el  código  ni  la  licencia,  dando  la  posibilidad  a  los desarrolladores  de  liberar  el  código  sin  perder  el  control  sobre sus creaciones o versiones; por lo que **cumple con las cuatro libertades del software**. 

Se  usa  principalmente  como  licencia  para  aplicaciones  de  Mozilla,  como  son  Firefox (navegador) o Thunderbird (gestor de correo), aunque también la usan otros programas como LibreOffice 4.0. 

#### **Copyleft** 

En este tipo de licencia, el propietario autoriza a copiar, modificar y distribuir, pero no permite agregar restricciones a la redistribución o modificación, que deben mantener el mismo tipo de licencia. 

![](SI23/docs/docs/img02/05.png)

#### **Apache** 

Licencia creada por Apache Software Foundation para  su  software,  aunque  en  realidad  hay muchos otros que hacen uso de ella.

![](SI23/docs/docs/img02/06.png)

Permite al usuario el uso sin restricciones,la distribución y la modificación. Sin embargo, no es copyleft ya que no exige que la distribución y las obras derivadas mantengan la licencia original. De esta manera, es posible que un software abierto en origen pueda convertirse en un software cerrado aplicando esta licencia. 

### Tipos de licencias de Sistemas Operativos 

En el caso de los sistemas operativos, predominan dos tipos de licencias: la licencia EULA (Windows) y la licencia GNU/GPL (Linux). 

#### Licencia EULA (licencia de usuario final)

Con esta licencia el producto solo puede ser utilizado por el usuario que lo ha adquirido. De  este  modo,  el  dueño  del  producto  obliga  al  usuario  final  a  reconocer  todas  las condiciones de la licencia, tales como las restricciones de uso, los derechos de autor y las  patentes,  así  como  la  posibilidad  de  que  el  propietario  recoja  información  del sistema y su uso. 

Esta licencia prohíbe la copia, y solo puede ser transferida una vez a otro usuario. Puede utilizarse solo en un equipo con un máximo de dos procesadores, que no sea servidor web ni de archivos. 

Si se efectúan cambios de hardware, puede dejar de funcionar y el usuario debe activar la licencia antes de 30 días desde su instalación. Tiene una garantía de 90 días, y no cubre las actualizaciones. 

Una de las polémicas de EULA es que el usuario en ningún momento es dueño del producto, únicamente dispone de una licencia de uso.

#### Licencia GNU/GPL 

Se  trata  de  la  primera  licencia  copyleft  de  uso  general,  lo  que  significa  que  las modificaciones realizadas sobre este tipo de software deben ser distribuidas bajo los términos de la misma licencia GNU/GPL. 

Permite  la  copia,  modificación y  redistribución  de  software,  proporcionando  garantía sobre los derechos del usuario tanto de copia como de modificación y redistribución. Garantiza a los usuarios los derechos del software libre, aunque el  trabajo sea modificado. 

Una patente sobre este tipo de software debe ser licenciada para el beneficio de la comunidad, y esta modificación no debe tener en ningún caso costo por la licencia. Además, debe incluir el código fuente del software desarrollado para dar al usuario la posibilidad de su modificación posterior, si así lo deseara.

### Distribución de licencias propietarias 

#### Retail

Está destinada a su venta directa al usuario final, aunque no está limitada a su equipo de destino, podemos venderla o cederla si desinstalamos el software de nuestro equipo. Sólo permite el uso en una sola máquina a la vez, se vende con su caja y manuales. El soporte técnico corre a cargo del fabricante.

#### OEM (Original Equipment Manufacturer)

Se encuentra ligada al equipo nuevo que se ha adquirido. No es posible vender/ceder la versión si no es con él. Es más barata que la licencia Retail, y el soporte técnico corre a cuenta  del  vendedor del  equipo.  Si el vendedor  nos  proporciona el software ya preinstalado en el equipo estaríamos hablando de licencia OEM por lotes. 

#### VLM (Volume License Manager)

Son las llamadas licencias por volumen y son una variante de la licencia OEM. Para una empresa con cientos de ordenadores, es complicado controlar las licencias individuales de cada una de sus máquinas. Existe la posibilidad de contratar un tipo de licencia especial con el desarrollador, de modo que, con una única clave de licencia, podemos utilizar varias máquinas a la vez. 

#### MSDN

Son licencias especiales para un uso educativo, por lo que siempre deben activarse en equipos que tengan una finalidad didáctica. También existen variantes para empresas de desarrollo, academias, etc.


## Sistemas Operativos Actuales

### Introducción

En  este  apartado,  abordaremos  los  principales  sistemas  operativos  que  existen actualmente en el mercado. No vamos a ceñirnos solamente en los sistemas operativos para equipos  de  sobremesa,  sino  que  también abordaremos  sistemas  operativos de dispositivos móviles. Pero antes de clasificarlos, vamos a estudiar qué es, cómo es y qué hace un sistema operativo. 

El sistema operativo es el conjunto de programas del sistema informático que controla los recursos hardware del ordenador y sirve de base para la ejecución de los programas de aplicación o de programación, se le considera el intermediario entre el hardware y los programas y usuarios.

Primero, vamos a realizar una **clasificación de los Sistemas operativos en función de su desarrollador:**

### Sistemas Operativos Linux

Los sistemas operativos Linux están desarrollados bajo la licencia GPL, por lo que se trata de un software libre, cuyo grado de libertad debe mantenerse en las diferentes distribuciones  de  este  software.  Estos  sistemas  están  desarrollados por una gran comunidad de empresas, asociaciones, colectivos e, incluso, por personas particulares. 

La base de este tipo de sistema es su núcleo o kernel. Partiendo de diferentes versiones del kernel junto con las evoluciones que se le integran, dan lugar a una enorme variedad de distribuciones. Actualmente pueden existir más de 500 distribuciones diferentes de Linux. En [Distrowatch](https://distrowatch.com) puedes ver las más importantes.

Las versiones sobre las que se sustentan la mayoría de distribuciones Linux actuales son: 

- Slackware: slackware Linux, Open SUSE, Slax, Vector Linux, etc. 
- Red Hat: Red hat Linux, CentOS, Mandriva, Fedora, etc. 
- Debian: debian, Ubuntu, Knoppix, Linux Mint, etc.
- Arch: Manjaro, Endevour, Arcolinux, Garuda, etc.

### Sistemas operativos Android

Este sistema es,  en  realidad,  una  distribución  de  Linux.  Diseñado  para  dispositivos móviles,  por  lo  que  se  ha  diseñado  para  arquitecturas  de  equipos ARM,  aunque  hay algunas distribuciones adaptadas a x86.

Las  distribuciones  de Android  son  únicas  para  todos  los  dispositivos  a  los  que  van dirigidas,  pero  en  función  del  dispositivo  (móvil,  Tablet, smartwatch,  etc)  usará  una versión u otra.

Android es desarrollado por Google, con el respaldo de la Open Handset Alliance, que es una  agrupación  de  compañías  para  el  desarrollo  de  estándares abiertos para dispositivos móviles. 

Los  nombres  de  las  versiones  de  Android  se  corresponden  con  golosinas  o  dulces, siendo la última versión conocida la Snow Cone (Android 12) lanzada en noviembre de 2022. 

### Sistemas Operativos Windows

Los sistemas operativos Windows se corresponden con una familia de distribuciones desarrolladas por la compañía Microsoft. Todos estos SS.OO. se distribuyen bajo licencia Microsoft  EULA  y  sólo  pueden  ser  desarrollados,  estudiados y modificados por esta compañía. 

Estos sistemas operativos son capaces de operar tanto en arquitecturas x86, como en ARM. El primer Windows surge en 1985 cuando Microsoft incorporó una interfaz gráfica a su sistema operativo MS-DOS.

Los sistemas Windows se basan principalmente en dos arquitecturas o familias: la 9X y la NT, aunque actualmente la que domina el mercado es la familia NT, un ejemplo de ello es el actual Windows 10. 

Ahora mismo podemos encontrarnos ordenadores con las siguientes versiones:  

- Para equipos basados en la arquitectura x86 o x64: podemos encontrar con equipos con Windows 7, Windows 8, Windows 10 y Windows 11, aunque Windows 10/11 son los únicos que tienen soporte estándar, el resto de sistemas se encuentra en [soporte extendido](https://support.microsoft.com/es-es/help/14085/fixed-lifecycle-policy) por lo que es conveniente dar el salto a la última versión de Windows.  
- Para equipos servidores: la última versión es Windows Server 2022. 
- Para  teléfonos  móviles:  existía una versión  llamada  Windows 10  Mobile, cuyo desarrollo fue suspendido por la poca cuota de mercado que tenía.  

El objetivo actual de Microsoft con su sistema operativo Windows 10/11 es el de conseguir un sistema operativo válido y eficiente para las diferentes arquitecturas y dispositivos existentes en el mercado.

### Sistemas operativos OS

Estos  sistemas  operativos  también  son  conocidos  como  **macOS**  y  pertenecen  a  la compañía Apple.  Esta  compañía  se  reserva  los  derechos  de  estudio y  desarrollo  del sistema operativo, por lo que es un **software privativo**, cuya licencia es Apple Public Source License / Apple EULA. 

En la actualidad tenemos las siguientes versiones disponibles: 

- Para los equipos de sobremesa: tenemos el sistema Mac OS X, sucesor del Mac OS 9. El OS X dispone de muchas versiones diferente siendo la más reciente Mac OS 13 de Junio de 2022 de nombre **Ventura**.
- Para equipos servidores: en estos equipos tiene una serie de versiones basadas en Unix, cuyo nombre es Mac OS X y dispone de varias versiones, siendo la más actual la versión 10.7 llamada “Lion” de 2011. Solo funciona con los antiguos servidores PowerPC.
- Para dispositivos móviles: los sistemas operativos de Apple para móviles y tablets de su marca se llaman iOS, cuya última versión es la 16.1, lanzada en octubre de 2022.

### Otros sistemas operativos

Además  de  estos  sistemas  operativos,  existen  otros  muchos  de  los  que  podemos destacar: 

- Google Chrome OS: Sistema Open Source desarrollado por Google y basado en Linux. Funciona en arquitecturas x86 y ARM.  
- Solaris: desarrollado inicialmente por Oracle, pero actualmente en su mayoría es de código abierto (Opensolaris). Su Kernel está basado en SunOs, que deriva de UNIX. Usa una interfaz gráfica basada en Java. 
- ***Berkeley Software Distribution*** o **BSD** (en español, «distribución de software Berkeley»)fue unsistema operativos derivado de [Unix](https://es.wikipedia.org/wiki/Unix) que nace a partir de los aportes realizados a ese sistema por la [Universidad de California en Berkeley](https://es.wikipedia.org/wiki/Universidad_de_California_en_Berkeley). Algunos sistemas operativos descendientes del sistema desarrollado por Berkeley son [SunOS](https://es.wikipedia.org/wiki/SunOS), [FreeBSD](https://es.wikipedia.org/wiki/FreeBSD), [NetBSD](https://es.wikipedia.org/wiki/NetBSD) y [OpenBSD](https://es.wikipedia.org/wiki/OpenBSD). Estos, a su vez, han sido utilizados por sistemas operativos propietarios, incluidos los macOS e iOS de Apple, que se derivaron de ellos, y Microsoft Windows que usaba (al menos) parte de su código TCP/IP, que era legal. El código de FreeBSD también se utilizó para crear el sistema operativo para la PlayStation y Nintendo Switch

## Clasificación de los Sistemas Operativos

El  sistema  operativo  es  un  programa  grande  y  complejo,  compuesto  por  unos componentes  con  las  funciones  bien  definidas.  Estos  componentes  se  pueden estructurar de distintas formas, haciendo que forme parte del kernel, o no. Por ello, vamos a hacer una primera clasificación de los sistemas operativos según su núcleo o kernel: 

- **Monolíticos:** no tienen una estructura clara y bien definida. Todos los componentes están  enlazados  en  un  único  programa  que  se  ejecuta  en  un  único  espacio  de direcciones. Todas  las funciones  se  ejecutan  en  modo  núcleo.  Parten  de  sistemas operativos sencillos a los que se les ha ido añadiendo muchas funcionalidades hasta convertirse en enormes y complejos. Los principales sistemas monolíticos son MS- DOS,  UNIX  y  todos  sus  derivados  GNU/Linux.  Su  principal  problema  es  que  son sistemas  poco  manejables  y  poco  comprensibles.  En  estos  sistemas  todos  los procedimientos y variables son visibles por todos. Para solucionar este problema, se necesita dotar de estructura al sistema operativo. 
- **Sistema  monolítico  por  capas**:  en  estos  sistemas,  cada  capa  implementa  una parte del sistema y las pone a la disposición de las capas superiores, tomando los  servicios  de  la  capa  inmediatamente  inferior.  Su  principal  ventaja  es  la modularidad  y  la  ocultación;  una  capa  no  tiene  que  saber  cómo  se  ha implementado  su  capa  inferior,  sólo tiene  que  conocer  la  interfaz  que  ofrece. Cada  capa  puede  construirse  y  depurarse  por  separado.  Algunos  ejemplos  de sistemas por capas son: THE, OS/2 y MULTICS. 
- **Microkernel  o  Cliente-Servidor:**  implementa  la  mayor  parte  de  los  servicios  y funciones del sistema operativo en procesos de usuario, dejando sólo una pequeña parte  del  sistema  operativo  ejecutando  en  modo  núcleo.  El  núcleo  realiza  unas funciones básicas que pueden variar, aunque suelen incluir la gestión de procesos, de memoria, la comunicación de procesos y la gestión de interrupciones; mientras que las demás funciones son servicios ofrecidos por los servidores, que se ejecutan en modo usuario. Este sistema presenta una gran flexibilidad, el fallo en un módulo no hace caer todo el sistema, es fácil de depurar. Sus principales desventajas son: es más difícil de construir ya que un módulo debe encajar con el resto, tienen mayor carga en el tratamiento de los servicios debido al uso de espacios de direcciones distintos, por lo que su rendimiento es menor. Algunos sistemas con este núcleo son: Minix, Amoeba y los actuales macOS. 

- **Híbridos:** Se trata de un micronúcleo al que se le han añadido algunos de los servicios no  esenciales  para  que  el  S.O.  trabaje  más  rápido.  Es  una  mezcla  entre  núcleo monolítico y micronúcleo. Algunos ejemplos de sistemas operativos con este tipo de núcleo son: los sistemas operativos Windows de la familia NT y DragonFly BSD.



![](OS-structure2.svg)

Otras posibles clasificaciones de los sistemas operativos según diferentes perspectivas son las mostradas a continuación:  



|**Número de usuarios**|**Número de tareas**|**Número de procesadores**|**Ofrecimiento de servicios**|
| :-: | :-: | :-: | :-: |
|Monousuario|Monotarea|Monoproceso|Centralizados|
|Multiusuario|Multitarea|Multiproceso|Distribuidos|
||||En red|
||||De escritorio|



## Principales funciones de los Sistemas Operativos

El sistema operativo está compuesto básicamente por tres capas: 

- El núcleo. (Kernel)
- Los servicios
- El intérprete de comandos.(Shell) 

![](SI23/docs/docs/img02/07.png)

El  **núcleo**  es  la  parte  del  sistema  operativo  que  interacciona  directamente  con  el hardware de la máquina. Sus principales funciones se centran en la gestión de recursos, como  el  procesador,  tratamiento  de  interrupciones  y  las  funciones  básicas  de manipulación de memoria.Hay diferentes tipos de kernels, como veremos más adelante. 

Los  **servicios** se agrupan según su funcionalidad en varios componentes, los cuales se ocupan de las **principales funciones** del sistema operativo. 

- **Gestión  de  procesos:**  se  encarga  de  la  creación,  planificación  y  destrucción  de procesos. 
- **Gestión de memoria:** gestiona las partes de memoria libres y ocupadas, así como de asignar y liberar la memoria para los diferentes procesos. 
- **Gestión de la E/S:** facilita la comunicación con los diferentes dispositivos periféricos. 
- **Gestión de archivos y directorios:** se encarga del manejo de archivos y directorios y de la administración del almacenamiento secundario. 
- **Comunicación  y  sincronización  entre  procesos:**  encargada  de  ofrecer mecanismos para que los procesos puedan comunicarse y sincronizarse. 
- **Seguridad y protección:** se encarga de garantizar la identidad de los usuarios y definir el nivel de permisos de acceso o modificación de los diferentes recursos del sistema. 

Estos  servicios  se  ofrecen  mediante  una  interfaz  de  llamadas  al  sistema  (*API  – Application  Programming  Interface*).  En  un  mismo  sistema  operativo  se  puede  incluir más de una API. Las APIs mostradas son: 

- **Windows API:** para los sistemas operativos Windows, también llamada Win32. 
- **POSIX:** para los sistemas operativos basados en UNIX, como las distribuciones GNU/ Linux. 
- **COCOAAPI:** interfaz para los últimos sistemas de macOS X, totalmente compatible con sistemas de 64 bits. 

El **Shell o intérprete de comandos** suministra una interfaz a través de la cual el usuario puede  interaccionar  con  la  computadora,  facilitando  el  acceso  a  las  funciones  del núcleo. El intérprete recibe las órdenes del usuario, los interpreta y, si es posible y está permitido, los ejecuta. Este intérprete en ocasiones se considera que forma parte del sistema operativo y en otras ocasiones no. Estos intérpretes pueden ser de varios tipos: 

- Interfaz gráfica de usuario **(*GUI - Graphic User Interface*)**
- Interfaz de línea de comandos **(Consola o terminal o *CLI - Command Line Interpreter*)**

El sistema operativo puede incluir varios interfaces, tanto en modo texto como gráficos, entre los cuales podemos optar según nos interese y disponibilidad.

## Gestión de procesos

### Introducción

Ya hemos dicho que el **núcleo** es la parte del sistema operativo que interacciona directamente con el hardware de la máquina. Una de las **principales funciones** del sistema operativo es la gestión de procesos, para ello se utilizan una serie de algoritmos que nacieron por la necesidad de poder ordenar los procesos para ganar eficiencia a la hora de tratar con ellos. Es decir, son los encargados de ordenar y dirigir los procesos para asegurar que ninguno de ellos monopolice el uso de la CPU.

### Conceptos básicos. 

Antes de ver algunos de los algoritmos más utilizados vamos a definir algunos conceptos básicos: 

- **Tiempo de espera**: el tiempo que un proceso permanece en espera en la cola de ejecución. 
- **Tiempo de retorno**: tiempo que va desde que se lanza un proceso hasta que finaliza. 
- **Tiempo de respuesta**: tiempo que un proceso bloqueado tarda en entrar en ejecución. 
- **Uso de CPU**: porcentaje de tiempo que la CPU está ocupada. 
- **Productividad**: número de procesos realizados en una unidad de tiempo. 

Por último, dos algoritmos: 

- **Apropiativo**: también conocido como expulsivo o expropiativo. Nos permite la expulsión de procesos para ejecutar un nuevo proceso, poniendo en cola al anterior. 
- **No apropiativo**: No nos permite la expulsión, por lo que un proceso nuevo no entrará hasta que termine el anterior. 

### Tipos de algoritmos. 

#### FCFS (First-Come, First-Served)

También llamado **FIFO** (First In, First Out). Este algoritmo es muy sencillo y simple, pero también el que menos rendimiento ofrece. Básicamente, en este algoritmo, el primer proceso que llega se ejecuta y, una vez finalizado se ejecuta el siguiente. **No apropiativo. Penaliza a los procesos cortos**. 

**Ejemplo:**

| **Procesos** | **Llegada** | **Tiempo uso CPU** |
| :----------: | :---------: | :----------------: |
|      P1      |      0      |         24         |
|      P2      |      2      |         3          |
|      P3      |      4      |         3          |




||0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|26|27|28|29|
|- |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|P1|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|F|||||||
|P2| | |E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|X|X|F| | | |
|P3| | | | |E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|E|X|X|F|

![image-20221104094128201](SI23/docs/docs/img02/08.png)

Tiempo de retorno = tiempo de finalización - tiempo de llegada

Tiempo de espera = tiempo de retorno - tiempo de servicio

#### SJF (Shortest Job First)

Este algoritmo siempre prioriza los procesos más cortos primero, independientemente de su llegada. En caso de que los procesos sean iguales, utilizará el método FIFO (es decir, el orden según su entrada). Este algoritmo corre el riesgo de poner siempre al final de la cola los procesos más largos, por lo que nunca se ejecutarán. Esto se conoce como **inanición**. Es un método **no apropiativo**. Solo se puede usar si se conoce de antemano la duración de cada trabajo. 

**Ejemplo:**

| **Procesos** | **Llegada** | **Tiempo uso CPU** |
| :----------: | :---------: | :----------------: |
|      P1      |      0      |         7          |
|      P2      |      2      |         4          |
|      P3      |      4      |         1          |
|      P4      |      5      |         4          |




||0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|
|- |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|P1|X|X|X|X|X|X|F| | | | | | | | | |
|P2| | |E|E|E|E|E|E|X|X|X|F| | | | |
|P3| | | | |E|E|E|F| | | | | | | | |
|P4| | | | | |E|E|E|E|E|E|E|X|X|X|F|



![image-20221104094649176](SI23/docs/docs/img02/09.png)

#### SRTF (Short Remaining Time Next)

**Si añadimos la expulsión** de procesos al algoritmo SJF, obtendremos el **SRTF**. Éste será capaz de expulsar un proceso largo en ejecución para ejecutar otros más cortos. El problema que puede surgir es que un proceso largo puede llegar a expulsarse muchas veces y nunca terminar debido a la ejecución de otros más cortos. 

**Ejemplo:** 

| **Procesos** | **Llegada** | **Tiempo uso CPU** |
| :----------: | :---------: | :----------------: |
|      P1      |      0      |         7          |
|      P2      |      2      |         4          |
|      P3      |      4      |         1          |
|      P4      |      5      |         4          |




||0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|
|- |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|P1|X|X|E|E|E|E|E|E|E|E|E|X|X|X|X|F|
|P2| | |X|X|E|X|F| | | | | | | | | |
|P3| | | | |F| | | | | | | | | | | |
|P4| | | | | |E|E|X|X|X|F| | | | | |



![image-20221104095505922](SI23/docs/docs/img02/10.png)

#### Round Robin

Este algoritmo asigna a cada proceso un tiempo equitativo tratando a todos los procesos por igual y con la misma prioridad. 

Este algoritmo es ***circular***, volviendo siempre al primer proceso una vez terminado con el último. Para controlar este método, a cada proceso se le asigna un intervalo de tiempo llamado **quantum** o **cuanto** (para definirlo se utiliza esta regla, el 80% de los procesos tienen que durar menos tiempo que el ***quantum*** definido). 

Pueden suceder dos casos con este método: 

- **El proceso es menor que el quantum**: al terminar antes, se planifica un nuevo proceso. 
- **El proceso es mayor que el quantum**: al terminar el quantum se expulsa el proceso dando paso al siguiente proceso en la lista. Al terminar la iteración se volverá para terminar el primer proceso expulsado. 

Algoritmo apropiativo. Se debe tener en cuenta que cada cambio de contexto genera retraso.

| **Procesos** | **Llegada** | **Tiempo uso CPU** |
| ------------ | ----------- | ------------------ |
| P1           | 0           | 10                 |
| P2           | 1           | 4                  |
| P3           | 2           | 3                  |



|| 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   | 12   | 13   | 14   | 15   | 16   |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| P1   | X    | X    | X    | X    | E    | E    | E    | E    | X    | X    | X    | X    | E    | E    | E    | X    | F    |
| P2   |      | E    | E    | E    | X    | X    | X    | F    |      |      |      |      |      |      |      |      |      |
| P3   |      |      | E    | E    | E    | E    | E    | E    | E    | E    | E    | E    | X    | X    | F    |      |      |

![image-20221104100203969](SI23/docs/docs/img02/11.png)

## Gestión de Memoria

En un sistema monoprogramado (lo contrario que multiprogramado), en la memoria del ordenador solo hay un único programa, acompañado de sus datos y del sistema operativo. Esto hace que el uso de la memoria, y la asignación de la misma al programa sea muy simple. Sin embargo, en un sistema multiprogramado nos vamos a encontrar en memoria con varios programas a la vez (2 en el mejor de los casos, pero podemos realizar multiprogramación con 20, 100 o 700 procesos). 

![](SI23/docs/docs/img02/12.jpeg)

Este “lio” que vemos en la memoria usando multiprogramación hace que se presenten dos problemas fundamentales, **la relocalización y la protección.**  

### Problemas con la memoria
#### Relocalización 

Consiste en que los programas que necesitan cargarse en memoria real ya están compilados y montados, de manera que internamente contienen una serie de referencias a direcciones de instrucciones, rutinas y procedimientos que ya no son válidas en el espacio de direcciones de memoria real de la sección en la que se carga el programa.  Esto  es,  cuando  se  compiló  el  programa  se  definieron  o  resolvieron  las direcciones de memoria de acuerdo a la sección de ese momento, pero si el programa se carga en otro día en una sección diferente, las direcciones reales ya no coinciden.  

Si en memoria solo va a estar este programa, no hay problemas en cargarlo siempre en la misma dirección o sección de memoria, pero si cargamos varios programas en la memoria, esto ya no es posible, dado que varios programas podrían pedir la misma sección. 

![](SI23/docs/docs/img02/13.png)

En este ejemplo teórico que vemos arriba, el proceso A está preparado para cargarse en la dirección de memoria 256.212. Mientras que solo dicho proceso esté funcionando en memoria no hay problema en esto.  

![](SI23/docs/docs/img02/14.png)

En este ejemplo teórico de arriba, vemos como al mismo tiempo que el proceso A, intentamos ejecutar un proceso B que quiere cargarse en la dirección de memoria 310.815... vemos como “machaca” al proceso A, y  también  sus  datos.  Esto  conllevaría  que  ambos  procesos  dejarían  de  funcionar,  ya  que  irían sobrescribiéndose el uno al otro.  

El **gestor** o **controlador de memoria** del sistema operativo, puede solucionar este problema de varias formas, una de las más usadas consiste en tener un **registro** que guarde la dirección **base** de la sección que va a contener al programa. Cada vez que el programa haga una referencia a una dirección de memoria, se le suma el registro base para encontrar la dirección real. Así, en el ejemplo anterior tendríamos que cuando el proceso A quiere acceder a la memoria para instalarse en la dirección 256.212, el SO (Sistema Operativo) hace la operación (dirección + base) donde base por ejemplo es 20.000 por lo que el proceso A sería cargado en la dirección 276.212. Cuando el proceso B se quiera cargar, el SO ajusta la base por ejemplo a 500.000 (para saltarse al proceso  A), de forma que en lugar de instalarse en la dirección 310.815 se instalará en la dirección 810.815.  

#### Protección 

Este problema se refiere a que, una vez que un programa ha sido cargado a memoria en algún segmento en particular, nada le impide al programador que intente direccionar (por error o deliberadamente) localidades de memoria menores que el límite inferior de su programa o superiores a la dirección mayor; es decir, quiere referenciar localidades fuera de su espacio de direcciones.  

![](15.jpeg)

Obviamente, este es un problema de protección, ya que no es legal leer o escribir en áreas de memoria que pertenezcan a otros programas, y hay que proteger estas zonas de memoria.  

La solución a este problema puede ser el uso de un **registro base** y un **registro límite**. El registro base contiene la dirección del comienzo de la sección que contiene el programa, mientras que el límite contiene la dirección donde termina. Cada vez que el programa hace una referencia a memoria se comprueba si cae en el rango de los registros y si no es así se envía un mensaje de error y se aborta el programa.  

Muchos  programas  antiguos  dan  errores  de  acceso  a  memoria  cuando  son  ejecutados  en  sistemas multiprogramados. Precisamente estos errores vienen dados porque intentan acceder a direcciones de memoria que quedan fuera de su ámbito.  

En estos casos, el sistema operativo impide que dichos programas accedan a esas direcciones, lo que provoca un error en el acceso a memoria.

![](16.jpeg)

### Memoria virtual

Las  CPU  de  los  ordenadores  eran  cada  vez  más poderosas, lo que permitía ejecutar programas cada  vez más potentes, y por lo tanto más grandes.

![](17.jpeg)

Al mismo tiempo, el uso de la multiprogramación, hacía  que  el  sistema  operativo  tuviera  que  colocar  por  decenas  de  estos  grandes  procesos  en  la memoria RAM.    

El  problema  es  que  la  cantidad  de  memoria  RAM  “física”  que  podemos  instalar  en  un  ordenador  es  finita,  es  decir,  tiene  un  límite.  Así,  si  intentamos  ejecutar en multiprogramación 20 procesos, y cada uno de ellos necesita 512 MB de RAM para trabajar, deberíamos tener instalados en nuestro main memory ordenador 10 GB de RAM.  

Todo esto empujó a los diseñadores de los sistemas operativos a implantar un mecanismo que permitiera ofrecer a los procesos más cantidad de memoria de la que realmente estaba instalada en la máquina, esto es, de ofrecer "**memoria virtual**”.  

La **memoria virtual** se llama así porque el programa ve una cantidad de memoria mucho mayor que la real, y que en realidad se trata de la suma de la memoria de almacenamiento primario y una cantidad determinada de almacenamiento secundario (por ejemplo, del disco duro).  

El sistema operativo, en su módulo de gestión de memoria, se encarga de intercambiar programas enteros, segmentos  o  páginas  entre  la  memoria  real  y  el  medio  de  almacenamiento  secundario.  Si  lo  que  se intercambia son procesos enteros, se habla entonces de **multiprogramación en memoria real**, pero si lo que se intercambian son segmentos o páginas, se puede hablar de **multiprogramación con memoria virtual**.  

Existe una técnica en la cual, el sistema operativo divide a los procesos en pequeñas porciones, de tamaño fijo denominadas **páginas**, de un tamaño múltiplo de 1 K. Estas páginas van a ser pasadas de la RAM al disco y viceversa. Al proceso de intercambiar páginas, segmentos o programas completos entre RAM y disco se le conoce como **'intercambio'** o ‘**swapping**".  

En la **paginación**, se debe cuidar el tamaño de las páginas, ya que si éstas son muy pequeñas el control por parte del sistema operativo para saber cuáles están en RAM y cuáles en disco, sus direcciones reales, etc, crece y provoca mucha "sobrecarga' (**overhead**). Por otro lado, si las páginas son muy grandes, el overhead disminuye, pero entonces puede ocurrir que se desperdicie memoria en procesos pequeños. Debe haber un equilibrio entre ambos conceptos.  

Otro aspecto importante es la estrategia para cargar páginas (o segmentos) a la memoria RAM. Se usan más comúnmente  dos  estrategias:  **cargado  de  páginas  por  demanda**  y  **cargado  de  páginas  anticipada.**  La estrategia de cargado y por demanda consiste en que las páginas solamente son llevadas a RAM si son solicitadas, es decir, si se hizo referencia a una dirección que cae dentro de ellas.  

La carga anticipada consiste en tratar de adivinar qué páginas serán solicitadas en el futuro inmediato y cargarlas de antemano, para que cuando se pidan ya no ocurran fallos de página. Ese "adivinar' puede ser que se aproveche del fenómeno de localidad y que las páginas que se cargan por anticipado sean aquellas que contienen direcciones contiguas a la dirección que se acaba de referenciar. En el caso de Windows, se usa una conjunción de ambos métodos, y se utiliza un fichero en disco duro donde se va almacenando toda la información sobre  índices de páginas en HD, en RAM, etc. Este fichero se denomina  **pagefile.sys**  y  lo  podéis  encontrar  normalmente  en  la  raíz  de  vuestro volumen de sistema.   

Un problema que tenemos con la memoria virtual es la diferencia  de velocidad enorme que existe entre la RAM y la memoria de  almacenamiento  secundario.  Si  cargamos  muchos  procesos,  y  agotamos nuestra memoria RAM real, el SO permitirá que todo  siga funcionando, usando el HD, pero tardará muchísimo en pasar  las páginas de RAM a HD y viceversa. En muchas ocasiones, nos  parecerá incluso que el SO se ha quedado “colgado”. Esto es muy  habitual en sistemas con poca memoria, donde vemos que de  repente la luz indicadora de actividad en los discos duros se queda  encendida, y el SO deja de responder durante un buen rato.   

Un intento de solucionar esto es usar memorias de estado sólido en lugar del HD para paginar ya que son memorias mucho más rápidas, esto fue implementado desde Windows Vista.  

## Sistema de Ficheros (FS.- File System)

Un fichero es un mecanismo de abstracción que sirve como unidad lógica de almacenamiento de información. El fichero agrupa una colección de informaciones relacionadas entre sí y definidas por su creador. A todo fichero le corresponde un nombre único que lo identifique entre los demás ficheros.   

Es necesario que el sistema operativo cuente con un sistema que se encargue de administrar la información almacenada en los dispositivos en forma de ficheros: de esto se encargan los sistemas de ficheros.   

Un sistema de ficheros es el aspecto más visible de todo sistema operativo y existe por razones tecnológicas, ya que no hay memoria principal lo suficientemente grande como para no necesitar de almacenamiento secundario. Surge debido a la necesidad del sistema operativo de poder gestionar la información de forma eficiente y estructurada, además de establecer unos parámetros de seguridad y protección en entornos críticos.  

El sistema operativo ofrece una visión lógica y uniforme del almacenamiento de información realizando una abstracción de las propiedades físicas de sus dispositivos de almacenamiento. Para ello, define el concepto lógico de fichero. El sistema operativo se debe encargar del acoplamiento entre los ficheros y los dispositivos físicos, por medio del sistema de ficheros, que debe ser independiente del soporte físico concreto sobre el que se encuentre.   

Los objetivos principales de todo sistema de ficheros deben ser los siguientes: Crear, borrar y modificar ficheros.  

- Permitir el acceso controlado a la información.  
- Permitir intercambiar datos entre ficheros.  
- Poder efectuar copias de seguridad recuperables. 
- Permitir el acceso a los ficheros mediante nombres simbólicos.   

Hay otros objetivos secundarios, entre los que destacan:   

- Optimizar el rendimiento.  
- Tener soportes diversos para E/S (para poder seguir utilizando los mismos ficheros, aunque cambie el soporte). 
- Ofrecer soporte multiusuario. 
- Minimizar las pérdidas de información.   

Normalmente los ficheros se organizan en directorios (también llamados carpetas) para facilitar su uso. Estos directorios son ficheros que contienen información sobre otros ficheros: no son más que contenedores de secuencias de registros, cada uno de los cuales posee información acerca de otros ficheros. 

La información que contiene un fichero la define su creador. Hay muchos tipos diferentes de información que puede almacenarse en un fichero: programas fuente, programas objeto, datos numéricos, textos, registros contables, fotografías, videos, etc. Un fichero tiene una cierta estructura, definida según el uso que se vaya a hacer de él.  

Por ejemplo, un fichero de texto es una secuencia de caracteres organizados en líneas (y posiblemente en páginas); un fichero fuente es una secuencia de subrutinas y funciones, un fichero gráfico es una secuencia que permite dibujar pixeles en pantalla, etc.  

Cualquier sistema operativo distingue entre varios **tipos básicos de ficheros**, que será la clasificación que consideremos nosotros: 

- **Regulares o Normales**: Aquellos ficheros que contienen datos (información).  
- **Directorios**: Aquellos ficheros cuyo contenido es información sobre otros ficheros, normalmente un vector de entradas con información sobre los otros ficheros. 
- **De dispositivo**: Existen dispositivos cuya E/S se realiza como si fuesen ficheros, por lo tanto, es razonable asociarles ficheros para simplificar y hacer más transparente el intercambio de información con dichos dispositivos.  

Aunque se imponga al sistema operativo el desconocimiento del tipo de ficheros que manipula, sí se hace una distinción del mismo de forma transparente: a través de las extensiones del nombre. Mediante la extensión del nombre del fichero (una cadena de caracteres de pequeña longitud) se puede determinar el tipo del fichero. Algunos sistemas de ficheros consideran a la extensión como una parte del nombre (y, de hecho, admiten que un mismo fichero posea varias extensiones anidadas), y otros la diferencian del nombre a nivel interno. 

De este modo, aunque el sistema operativo no conozca internamente la estructura de los ficheros, si es capaz de manejarlos eficientemente gracias al uso de estas extensiones. Esta es la aproximación de los sistemas operativos de Microsoft. 

Unix y sus variantes (Linux) sin embargo, optan por la no utilización de extensiones, lo que implica que el usuario es el único encargado de saber lo que se puede realizar o no con un fichero dado.   

10.1 ESTRUCTURAS DE DIRECTORIOS.  

Veamos el siguiente ejemplo: Imaginemos un bufete de abogados que dispone de una ingente cantidad de información en papel: casos judiciales, precedentes, historiales de abogados, historiales de clientes, nóminas, cartas recibidas, copias de cartas enviadas, facturas del alquiler del local, albaranes de compra de lapiceros, procedimientos, etc.   

Ahora supongamos que todos estos documentos se almacenan en una enorme montaña de papel en el centro de  una  habitación:  la  locura  está  garantizada.  Obviamente  el  bufete  debe  disponer  de  un  armario  de archivadores, la información se podrá almacenar de forma lógica para poder acceder a ella rápidamente cuando sea necesario.   

Lo mismo ocurre en un sistema de ficheros informático: conviene guardar la información (los ficheros) en archivadores. Los archivadores serán lo que llamaremos directorios, un tipo especial de ficheros donde se almacena información relativa a otros ficheros.   

Así, en un directorio se almacenarán ficheros relacionados entre sí, y ficheros totalmente independientes irán alojados en distintos directorios. Evidentemente, esta organización es puramente lógica: todos los ficheros estarán almacenados físicamente en el mismo lugar.   

Hay varias formas de organizar los directorios sobre un disco: 

![](18.png)

- **Directorio de un nivel.** En este tipo de organización solo se permite  un nivel de directorio.   
- **Directorio de dos niveles.** En este tipo de organización, un directorio  puede incluir dentro otro directorio, pero este ya no puede incluir  otro más.  
- **Directorio  con  estructura  arborescente.**  Prácticamente  no  tiene  limitaciones.  Un  directorio  puede  incluir  otros  directorios,  sin  importar su número, y estos nuevos directorios pueden contener  otros directorios.    

De esta forma, cada usuario puede crear sus propios directorios para organizar sus ficheros a su gusto. Un ejemplo de estructura de directorios de esta forma es la considerada por los sistemas de ficheros de Unix, MS-DOS, Windows, etc.   

El árbol es de raíz única, de modo que cada fichero tiene un único nombre de ruta de acceso. El nombre de ruta  de  acceso  en  un  directorio  de  esta  forma  es  la  concatenación  de  los  nombres  de  directorio  y subdirectorios desde el directorio raíz hasta el directorio donde se encuentra alojado el fichero a través del camino único, culminando con el propio nombre del fichero dentro del directorio. 

Un directorio (o subdirectorio) contiene a su vez ficheros y/o subdirectorios, y todos los directorios poseen el mismo formato interno. Las entradas del directorio indican si el objeto referenciado es un fichero o un subdirectorio.   

Se define **directorio padre** de un fichero o subdirectorio como el directorio en el que se encuentra su entrada de referencia Cada fichero o directorio (a excepción del directorio raíz) posee un único directorio padre. El directorio padre suele ser referenciado por los sistemas operativos con punto punto (..).   

Se define directorio hijo de un directorio como el directorio que tiene por padre al primero. Un directorio puede contener múltiples directorios hijos, y cada directorio (a excepción del raíz) es hijo de algún otro.   

Se define **directorio actual** como aquel en el que trabaja el usuario por defecto. Suele ser referenciado por los sistemas operativos con un punto (.). Cuando el usuario hace referencia a un fichero por nombre (no por nombre de ruta de acceso), el sistema inicia la búsqueda siempre en el directorio actual. Si no lo encuentra, comienza a recorrer el camino de búsqueda hasta dar con él. El usuario puede referirse a un fichero también por su nombre de ruta de acceso, en cuyo caso no se da lugar a emplear el camino de búsqueda. El usuario también puede cambiar su directorio actual, especificando un nombre de directorio.   

En este caso, los nombres de ruta de acceso pueden adoptar dos formas alternativas.  

La primera es la del nombre de **ruta absoluto**, la que hemos definido, por la cual se nombra a cada fichero con respecto al directorio raíz.   

![](19.png)

Por ejemplo, un nombre de ruta absoluto válido es C:  

`\Documentos\Jose\Privado\Carta.txt`. Normalmente, se denota el directorio raíz por medio de un símbolo especial dependiente de cada sistema de ficheros, aunque los más habituales son los símbolos '/' y '\'. En una estructura de directorio de este tipo, el nombre de ruta de acceso absoluto de un fichero o directorio debe ser único.   

La segunda opción es la del nombre de **ruta relativo**. En este caso, se nombra al fichero con respecto al directorio actual. Para esta labor se definen en cada directorio dos entradas de directorio especiales: `.` (Un punto) que representa al propio directorio y `..` (Dos puntos), que representa a su directorio padre. Así, se puede considerar un camino único desde el directorio actual hasta cualquier fichero o directorio del sistema. Un ejemplo de ruta relativa válida podría ser por ejemplo `..\Privado\Carta.txt` o `Jose\Privado\Carta.txt`.   

Los ficheros se van almacenando en el dispositivo, y por cada uno de ellos se apunta una entrada de directorio, donde almacenamos información sobre el tipo de fichero, nombre y demás. Hay que notar que por cada fichero se almacena por un lado el propio fichero, los datos, y por otro lado se almacena esta entrada de directorio.  

Pero ¿qué se almacena realmente en una entrada de directorio? La siguiente tabla muestra algunas de estas informaciones, aunque en un sistema de ficheros concreto pueden no estar todas las que son ni ser todas las que están:   


|Atributo|Cometido|
|-|-|
| Nombre del fichero | El nombre simbólico del fichero |
| Tipo de fichero    | Para aquellos sistemas que contemplan diferentes tipos |
| Ubicación                                                    | Un puntero al dispositivo y a la posición del fichero en el dispositivo. |
| Tamaño                                                       | Tamaño actual del fichero (en bytes, palabras o bloques) y el máximo tamaño permitido. |
| Posición actual                                              | Un puntero a la posición actual de lectura o escritura sobre el fichero. Su lugar exacto en el dispositivo. |
| Protección                                                   | Información referente a los permisos de acceso al fichero.   |
| Contador de uso                                              | Número de procesos que están utilizando simultáneamente el fichero. |
| Hora y fecha                                                 | De creación, último acceso, etc.                             |
| Identificación                                               | Del proceso creador del fichero, del último que accedió al fichero, en qué forma lo hizo, etc. |
| 
Según el sistema concreto, una entrada de directorio puede ocupar desde una decena hasta varios miles de bytes. Por esta razón, la estructura de directorios suele almacenarse en el propio dispositivo que se está organizando, como un fichero especial.  La forma de almacenar los directorios en el dispositivo (estructura de datos del directorio) varía también de un sistema a otro. La forma más sencilla es la de una ***lista lineal***, de forma que cada entrada se encuentra inmediatamente a continuación de la precedente. Esto sin embargo es muy caro en ejecución, pues la búsqueda de una entrada concreta suele exigir pasar por todas las anteriores (búsqueda lineal). Hay otros problemas, como el de qué hacer cuando se elimine una entrada (algunos sistemas la marcan como borrada para su posterior utilización, otros la incluyen en una lista de entradas libres). |                                                              |

Otra opción es mantener una ***lista lineal ordenada***, pero exige el mantener permanentemente ordenada la lista lo que complica excesivamente las operaciones de borrado y creación de entradas y la complicación del algoritmo de búsqueda. Puede pensarse entonces en emplear un ***árbol binario de búsqueda***, que simplifica las operaciones antes mencionadas (y complica el algoritmo de búsqueda). 


## Capas
Las imágenes se construyen sobre una tecnología de **sistema de ficheros por capas**.
Para crear una imagen, generalmente se crea el archivo de texto `dockerfile` formado por diferentes **instrucciones**. Cada línea representa una instrucción, y cada vez que se ejecuta el dockerfile se ejecutan dichas instrucciones de arriba a abajo.
Estos `dockerfile`-s se almacenan como texto y se pueden compartir con facilidad, así como almacenarse en sistemas de control de versiones.
Cada **instrucción** que se ejecuta cambia ligeramente el estado del sistema de archivos respecto a la instrucción anterior.
La diferencia entre el estado del sistema de ficheros antes y después de cada instrucción se guarda en disco como un archivo, que conforma una **capa**.
Cada **imagen** es un conjunto de capas que contienen los diferentes cambios que se van realizando sobre el sistema de archivos empaquetados.
Al final del `dockerfile`, la última instrucción define el **comando** que se ejecutará cuando arranquemos el contenedor.
Al ejecutar un comando a partir de la imagen creada, se ejecuta el comando especificado y se convierte en el proceso con PID 1 dentro del árbol virtual de procesos.
El contenedor seguirá en marcha mientras el proceso creado siga en ejecución.

## Capas
Las imágenes se construyen sobre una tecnología de **sistema de ficheros por capas**.
Para crear una imagen, generalmente se crea el archivo de texto `dockerfile` formado por diferentes **instrucciones**. Cada línea representa una instrucción, y cada vez que se ejecuta el dockerfile se ejecutan dichas instrucciones de arriba a abajo.
Estos `dockerfile`-s se almacenan como texto y se pueden compartir con facilidad, así como almacenarse en sistemas de control de versiones.
Cada **instrucción** que se ejecuta cambia ligeramente el estado del sistema de archivos respecto a la instrucción anterior.
La diferencia entre el estado del sistema de ficheros antes y después de cada instrucción se guarda en disco como un archivo, que conforma una **capa**.
Cada **imagen** es un conjunto de capas que contienen los diferentes cambios que se van realizando sobre el sistema de archivos empaquetados.
Al final del `dockerfile`, la última instrucción define el **comando** que se ejecutará cuando arranquemos el contenedor.
Al ejecutar un comando a partir de la imagen creada, se ejecuta el comando especificado y se convierte en el proceso con PID 1 dentro del árbol virtual de procesos.
El contenedor seguirá en marcha mientras el proceso creado siga en ejecución.