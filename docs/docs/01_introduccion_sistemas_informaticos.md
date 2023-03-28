# Introducción a los Sistemas Informáticos

## FUNDAMENTOS DE LOS SISTEMAS INFORMÁTICOS Y LAS MÁQUINAS VIRTUALES 

Objetivos: 

- Aprender cuáles son y cómo actúan las unidades funcionales de un sistema informático. 
- Conocer las funciones de los principales componentes físicos de un sistema informático. 
- Reconocer  los  componentes  físicos  de  un  sistema  informático  y  mecanismos  de interconexión. 
- Verificar el proceso de puesta en marcha del equipo. 
- Clasificar, instalar y configurar diferentes dispositivos periféricos. 
- Conocer el concepto de máquina virtual y sus ventajas- 
- Operar  las  máquinas  respetando  las  normas  de  seguridad  y  las  recomendaciones ergonómicas. 

Arquitectura de un sistema informático. Modelos. 

Un **sistema informático** es una máquina que acepta unos datos de entrada, los procesa y genera unos resultados. En todo sistema informático se distinguen dos partes claramente diferenciadas y necesarias: 

- **Hardware**: conjunto de elementos físicamente tangibles. 
- **Software**:  parte  intangible  formada  por  instrucciones  o  datos  que  pueden  ser interpretados o procesados. 

Los sistemas informáticos actuales tienen como base las arquitecturas de  *Von Neumann y Harvard*. 

El modelo de Von Neumann consta de las siguientes partes: 

1 **Unidad de procesamiento**: se encarga de la ejecución e interpretación de instrucciones y datos formada por unidad aritmético lógica (ALU), unidad de control y registros de almacenamiento. 

1) **Memoria**: almacena instrucciones y datos. 
1) **Dispositivos de entrada/salida**: elementos que actúan de interfaz con el resto de las partes. 

![01](SI23/docs/docs/img01/01.png)

En el modelo de Von Neumann las diferentes unidades funcionales se interconectan mediante buses de comunicación o buses del sistema. Estos pueden ser: 

- **Buses de instrucciones:** líneas de comunicación que transmiten instrucciones. 
- **Buses de datos:** líneas de comunicación que transmiten únicamente datos. 
- **Buses de direcciones:** líneas de comunicación empleadas para acceder a las distintas memorias, indicando una dirección de acceso de lectura o escritura. 

En  el  modelo  Harvard  el  acceso  a  datos  e  instrucciones  se  realiza  simultáneamente  al encontrarse en caminos distintos. 

## Componentes hardware de un sistema informático. 

El hardware de un equipo consta de multitud de componentes, los más importantes son: el microprocesador,  la  placa  base,  la  memoria  principal,  los  dispositivos  de  almacenamiento secundario, la batería o fuente de alimentación y los periféricos. 

### Microprocesador

El microprocesador es un circuito integrado encapsulado de altísimo nivel de integración en los componentes que aloja. El microprocesador contiene una o más unidades centrales de proceso (CPU). Este es el centro neurálgico de procesamiento del sistema. Las partes más importantes de una CPU son las siguientes: 

1) **Unidad de control (UC):** encargada del procesamiento, interpretación y ejecución de instrucciones y datos.  Envía al resto de componentes señales de control, estado o situación para la correcta automatización de las diferentes funciones del sistema de manera sincronizada. 
1) **Unidad aritmético lógica (UAL):** componente encargado de realizar cálculos aritméticos y lógicos. 
1) **Registros:** memorias *temporales* de poca capacidad y alta velocidad. 

Los microprocesadores actuales alojan la CPU, además de otros muchos elementos. Los más importantes son: 

- **Núcleo**: estructura que aloja las unidades funcionales de una CPU. En la actualidad, es común que los micros contengan más de un núcleo. Cada núcleo es capaz de ejecutar una  instrucción,  sincronizándose  con  el  resto  para  realizar  varias  tareas simultáneamente. 
- **Memorias caché**: memorias temporales, extremadamente rápidas y cercanas al núcleo. Atendiendo a su cercanía con este, suelen encontrarse tres niveles: 
- **L1 o de nivel 1**: normalmente situada dentro de cada núcleo. 
- **L2 o de nivel 2**: suele estar situada fuera de los núcleos, pero compartida entre varios. Actúa de intermediaria de los niveles L1 y L3. 
- **L3 o de nivel 3**: suele estar situada fuera de los núcleos, pero compartida por todos ellos. Este nivel recibe o entrega instrucciones y datos a o desde los módulos de memoria. 
- **Controlador de memoria**: la memoria RAM es gestionada por este componente. 
- **Controlador gráfico**: hace referencia a la capacidad de computación de cálculo para gráficos. No todos los procesadores integran esta característica, puesto que las tarjetas gráficas dedicadas a este propósito poseen mayor rendimiento.

En cuanto a las características más importantes de los procesadores, destacan: 

1. *Velocidad o frecuencia:* medida en gigahercios (GHz), hace referencia al número de ciclos que tienen que transcurrir para ejecutar una instrucción o parte de ella en cada CPU. A mayor frecuencia, mayor velocidad de procesamiento. 
1. *Número  de  hilos:*  los  procesadores  pueden  ejecutar,  al  mismo  tiempo,  hilos  de procesamiento, es decir, tareas como parte de un mismo proceso. Este concepto se refiere al número de hilos con los que los núcleos del procesador son capaces de trabajar en paralelo. 
1. *Nivel de integración:* hace referencia a la medida de nanómetros (nm) empleados para la fabricación del procesador, aplicando técnicas litográficas. Cuanto menor sea esta cantidad, mayor nivel de integración tendrá al poder incluir en el mismo espacio mayor número de componentes. 
1. *Consumo:* medido en watios (W), depende del voltaje e intensidad que necesite el procesador.  
1. *Potencia de disipación térmica (TDP):* hace referencia a watios térmicos, con objeto de buscar una solución de refrigeración al procesador. Los equipos móviles se distinguen claramente por su bajo TDP. 

Link: [¿Por qué la relación entre CPU, RAM y almacenamiento decide el rendimiento?](https://territoriointel.xataka.com/que-relacion-cpu-ram-almacenamiento-decide-rendimiento/?utm_source=Outbrain&utm_medium=Discovery&utm_campaign=BTS-Jim-Parsons&utm_content=)

### Memoria principal

La memoria de almacenamiento principal se encuentra conectada a la CPU, a la cual abastece almacenando instrucciones o datos de forma temporal, es decir, cuando carece de energía, su contenido desaparece. 

La memoria principal engloba varios tipos de memoria: registros, memoria caché y memoria RAM.
![02](SI23/docs/docs/img01/02.png)
La memoria principal está constituida por: 

1) ***Registros***: estructuras de almacenamiento pertenecientes al núcleo de la CPU de muy poca capacidad, pero cuyo acceso y escritura es extremadamente rápido. La mayoría se encuentran en la UC y la UAL. El tamaño de los registros define la arquitectura, siendo de 32 o 64 bits.

2) ***Memoria caché***: memoria intermedia entre los registros y la memoria RAM, que se encuentra en los núcleos o en el microprocesador. Cuanto mayor es su capacidad, mayor capacidad de cómputo tendrá el micro, ya que disminuirán las veces que esta tenga  que  recargarse  accediendo  a  la  memoria  RAM  y  volcar  nuevos  datos  o instrucciones.  Suelen  existir  tres  niveles  (L1,  L2  y  L3),  donde  se  alojan  de  manera compartida o  separada  las  instrucciones y  los  datos.  Es  común  que  se  encuentren separados en algún nivel para aumentar la velocidad de procesamiento, normalmente en L2 y L1. 

4) ***Memoria  RAM***:  memoria  externa  al  microprocesador  que  se  agrupa  en  forma  de módulos de memoria instalados en la placa base. Sus principales características son: 

5. ***Capacidad***: tamaño especificado en gigabytes (GB). 
6. ***Velocidad***:  frecuencia  de  trabajo  interna  de  cada  módulo.  Se  mide  en gigahercios (GHz). 
7. ***Voltaje***: tensión necesaria para su funcionamiento (V). 
8. ***Latencias***: especifica los tiempos de acceso a los datos de los chips del módulo de memoria. Cuanto menor sean las latencias, más velocidad tendrá el módulo en localizar y disponer de los datos. Se mide en ciclos de reloj. 
9. ***Número de canales de comunicación con el procesador***: el número de canales entre la memoria y el procesador para transferir información simultáneamente. Los módulos deben estar desarrollados con tecnología multicanal. Para ello, es necesario emplear parejas o cuartetos de módulos, respectivamente. Esto hará que se incremente la velocidad de transferencia al trabajar el procesador en paralelo con varios módulos. 
10. ***Tipo de módulo***: los chips de memoria se encapsulan en módulos DIMM o SODIMM, según sean para equipos de sobremesa o portátiles respectivamente. 
11. ***Tecnología***: los módulos de memoria actuales emplean una tecnología de tipo SDRAM DDR4. Son memorias de acceso aleatorio dinámico (DRAM), empleando doble recarga en su versión 4 (DDR4). En la siguiente figura, la muesca situada entre los contactos metálicos, en la parte inferior de cada módulo, se encuentra en posiciones distintas para evitar errores en la colocación de los módulos sobre los zócalos de memoria. Los módulos de memoria con tecnología SDRAM-DDR4 ofrecen mejoras con respecto a sus predecesoras SDRAM-DDR3: menos voltaje, mayor frecuencia, aumentan la densidad de los chips de memoria y presentan un mayor ahorro energético. 


![03](SI23/docs/docs/img01/03.png)


### Placa base 

También llamada ***motherboard***. La placa base es el circuito impreso principal de todo sistema informático, que conecta todos los componentes hardware directa o indirectamente. Se puede considerar la pieza fundamental (junto con la CPU), ya que determina la potencia de cálculo o procesamiento, la capacidad de expansión, el almacenamiento, el tipo de alimentación o el tipo de caja. 

Las placas base se rigen por los llamados ***factores de forma***. Estos determinan entre otros aspectos, las medidas de la placa, la disposición y lugar donde se alojan sus componentes (zócalos, conectores, buses de expansión), la potencia… 

Los factores de forma más utilizados son: 

- ***ATX***. La disposición de sus componentes mejora la refrigeración. Es el más utilizado actualmente.  Presenta  variantes  como  Micro-ATX  o  Mini-ATX,  que  reducen  las dimensiones de las placas base y están orientadas a equipos menos potentes, reducido consumo y escasa capacidad de expansión. 
- ***Variantes ITX***. Orientados a equipos de muy bajo consumo y reducidas dimensiones. Prácticamente  todos  sus  componentes  están  integrados  en  la  misma  placa  base, consiguiendo reducir las dimensiones, pero afectando a su capacidad de expansión.

Los principales componentes de una placa base son: 

#### Chipset 

Es  el  principal  circuito  integrado  y  encapsulado  (microchip)  en  la  placa  base,  que  resulta fácilmente distinguible por su tamaño y localización. 

![](SI23/docs/docs/img01/04.png)

Su labor es gestionar todos los componentes  de la placa base, dotándolos de sincronismo  a través de diferentes buses. Por ello, directa  o indirectamente,  el  chipset  siempre  interviene en cualquier operación. Tanto es  así, que éste determina el procesador que se  puede instalar en la placa base, la memoria  RAM, la cantidad de buses disponibles para  ranuras  de  expansión,  el  arranque  del  sistema,  la  cantidad  y  tipos  de  conectores  internos  y  externos,  la  capacidad  de  overclocking, etc. 

Las funciones del chipset son: 

- Coordinar  la  asociación  entre  los  componentes  de  gran  capacidad  de transferencia de información o procesamiento, como el procesador, la memoria, buses PCI Express de gráficos. 
- Actuar  de  concentrador  de  componentes  de  entrada  y  salida,  así como  de dispositivos de baja velocidad. 

En las placas base ATX, el chipset se sitúa al sureste del zócalo del procesador y son fácilmente distinguibles al ser chips grandes y disponer de un gran disipador. 

#### Zócalo del microprocesador 

El socket o zócalo del micro es el lugar donde se inserta éste. Existen principalmente dos tipos: 

- ***ZIF  o  PGA  (Pin  Grid  Array):***  consiste  en  una  estructura  de  plástico  con  pequeños agujeros, donde se insertan las patillas del microprocesador. Este se coloca en el socket sin ejercer presión, ya que dispone de una palanca para encajarlo sin fuerza. 

![](SI23/docs/docs/img01/05.png)

- ***LGA (Land Grid Array):*** dispone de una base con contactos que se comunican con la placa  base, sobre  la  que cierra  una estructura  de metal  con  forma  de ventana.  El procesador dispone de contactos y no patillas, por lo que establece la comunicación por presión gracias a dicha estructura. La instalación en este socket es sencilla, con mucho menos riesgo de dañar el micro. Permite mayor cantidad de contactos. 

#### Ranuras de memoria RAM 

![](SI23/docs/docs/img01/06.png)


Las ranuras de memoria son espacios destinados a alojar los módulos de memoria RAM. Actualmente, los  más utilizados son ranuras DIMM SDRAM-DDR4 con  288 pines. Todas las ranuras disponen de una marca  para  alinear  el  módulo  correctamente,  así  como  contenedores laterales para aumentar la sujeción de  este a la placa base.   

Las  placas  base  disponen  de  tecnología  de  doble,  triple  o  cuádruple  canal  (llamadas  ***Dual  Channel,  Triple  Channel  o  Quad  Channel***).  Así,  se  consigue  acceder  a  varios  módulos  simultáneamente,  mejorando la velocidad de acceso a la memoria RAM  por  parte  del  procesador.  Ello  gracias  a  duplicar,  triplicar o cuadruplicar el canal de 64 bits del ***single  channel*** por defecto.  

Las  placas  base  presentan  las  ranuras  de  memoria  RAM asociadas con colores (parejas, tríos o cuartetos)  para hacer uso de esta característica.  

#### Ranuras de expansión 

![](SI23/docs/docs/img01/07.png)


Son los módulos encargados de alojar las  tarjetas  de  expansión  para  ampliar  las  características del equipo. Según el ancho  de  banda  y  la  velocidad  de  transmisión,  encontramos  varios  tipos  de  buses  de  expansión,  los  cuales  emplean  diferentes  ranuras.  El  bus  más  empleado  es  el  PCI  Express, o PCIe, que se implementa hasta  con 16 líneas (lanes) de datos. Cada línea  dispone de un ancho de banda de 2GB/s en  su versión 4.0. Las ranuras de expansión PCI  Express más comunes según sus lanes y su  ancho de banda son:  

- PCIe x1 v4.0:2 GB/s 
- PCIe x4 v4.0:16 GB/s 
- PCIe x16 v4.0:32 GB/s 

Las distintas versiones de PCIe son compatibles entre sí. Se emplean para alojar tarjetas gráficas, tarjetas de sonido, dispositivos de almacenamiento secundario, tarjetas adaptadoras de red, etc. 

#### BIOS (Basic Input Output System)

También llamado ROM BIOS. Es un chip que se encuentra físicamente visible en la placa base y se encarga de varias tareas: 

- Comprobar el sistema y lanzar su arranque. 
- Realizar funciones básicas de E/S con el sistema operativo funcionando. 
- Configurar el equipo a través de una aplicación llamada BIOS Setup Utility. 

Muchas placas disponen de dos BIOS. En caso de que una se corrompa, la otra se activa, impidiendo que el equipo deje de funcionar. 

La BIOS tiene asociada una memoria RAM-CMOS que almacena de manera temporal los datos de la configuración del sistema. Estos datos aparecen cuando accedemos al BIOS Setup Utility: fecha y hora del sistema, medios de arranque, periféricos, buses, overclocking, chipsets… 

Al ser la RAM-CMOS una memoria volátil, la placa base tiene una pila que la alimenta e impide que desaparezca su configuración. Si la pila pierde su carga, es necesario ajustar algunos de estos valores para que el sistema arranque correctamente. 

Las placas base también disponen de unos pines o botones para resetear la memoria RAM- CMOS, si se desea volver a ajustar la configuración del sistema a la versión de fábrica.

![](SI23/docs/docs/img01/08.png) 

En la foto puede distinguirse:

- La pila

- Sistema de doble BIOS (backup Bios y Main Bios) 

- Pines de reseteo de la memoria 

#### Conectores internos 

Algunos de los conectores más importantes son: 

- *Conector  SATA:*  empleado  para  la  transferencia  de  datos  entre  el  chipset  y  los dispositivos de almacenamiento secundario. Es el conector que más se utiliza para conectar discos duros. Sustituyó al antiguo IDE. 
- *Conector  M.*2:  se  usa  especialmente  para  almacenamiento  (discos  duros  SSD)  o conectividad en equipos de reducidas dimensiones, aprovechando el espacio en la placa base. Trabaja con buses SATA o PCIe, empleando distintos conectores cada uno de ellos. 
- *Conectores de ventiladores:* los ventiladores refrigeran el procesador, la caja o incluso algunos chipsets. 
- *Conectores USB:* encargados de conectar, a través de un cable, los conectores USB del frontal de la caja de los equipos. 

![](12.png)

- *Conectores del panel frontal:* se suelen presentar por colores, detallando en la placa base la correspondencia de cada conector. Los más empleados son: 
- *Botón de encendido.* 
- *Botón de reset.* 
- *Led de encendido.* 
- *Led de uso de disco duro.* 
- *Conectores de alimentación:* nutren de energía eléctrica a la placa base y a todos sus componentes.  Es  habitual  encontrar  un  conector  de  20 o  24  pines  que  suministra alimentación a la placa base, y otro de 4 u 8 pines que alimenta al procesador (se encuentra cerca). 

![](SI23/docs/docs/img01/13.png)

#### Conectores externos 

La conexión entre periféricos y el equipo se realiza a través de conectores de comunicación externos anclados al lateral oeste de la placa base. Estos conectores utilizan diferentes buses de comunicación hacia el chipset. 

Los principales conectores externos son: 

- ***eSATA***: utilizado para conectar dispositivos de almacenamiento externo. 
- ***Thunderbolt***: para conectar periféricos de almacenamiento o para transmitir vídeo a periféricos. Emplea tecnología óptica. 

![](SI23/docs/docs/img01/14.png)

- ***USB***: conector empleado para conectar periféricos, ratón, teclado, impresora, discos duros externos, smartphones… Existen varias versiones de este conector. 

![](15.png)

- ***Conectores de vídeo***: transmiten señales de vídeo a monitores. Los más empleados son D-SUB (VGA),  DVI, Displayport y  HDMI  (los  dos  últimos también  pueden  transmitir audio). 
- ***Conector Ethernet LAN***: llamado también RJ45, empleado para comunicarse por cable de par trenzado en una red. 
- ***Conectores  de  audio  Jack  y  S/PDIF***:  transmiten  sonido  analógico  y  digital respectivamente. 
- ***Conectores PS/2***: para conectar teclados y ratones. 

![](16.png)

### Dispositivos de almacenamiento secundario 

Se emplean  para  almacenar  información  de  manera  permanente.  Hay  que  distinguir  los dispositivos de los medios, ya que los primeros alojan a los segundos, los cuales contienen la información.  Pueden  estar  juntos  (discos  duros  mecánicos)  o  separados  (tarjeta  Flash  SD necesita un lector de tarjetas SD para leer o escribir en ella). Los principales dispositivos o medios de almacenamiento no volátil se clasifican en: 

#### Medios de almacenamiento Flash 

Casi todos estos tipos de medios emplean tecnología Flash NAND, haciendo referencia a las puertas lógicas que almacenan los bits. Por ejemplo: 

- ***Disco  duro  SSD  (Solid  State  Drive):***  dispositivo  de  estado  sólido,  llamado  así  en contraposición a los discos duros magnéticos que presentan partes móviles. 
- ***Tarjetas de memoria:*** aunque existe multitud de tipos y con distintas capacidades, las más utilizadas son las SD y CompactFlash, en sus diferentes formatos. Los dispositivos donde se utilizan suelen ser portátiles, es decir, cámaras de fotos, móviles, consolas… 

![](017.png)

Dispositivos de almacenamiento magnético 

- ***Disco duro mecánico:*** formado por un conjunto de discos de material rígido apilados sobre el mismo eje rotatorio. Cada disco consta de dos caras con pistas concéntricas en cada una, susceptibles de ser magnetizadas y alterar así su estado, para almacenar ceros o unos. Entre cada cara se encuentran los cabezales de lectura y escritura que actúan sobre las pistas. 

![](018.png)

- ***Cintas:*** medio de almacenamiento formado por una banda de plástico flexible que contiene pistas aptas de ser magnetizadas y que se recoge sobre sí para distribuirlo o almacenarlo de forma segura. Estos medios de almacenamiento se utilizan en centros de  procesos  de  datos  como  formas  de  *backup*,  ya  que  son  económicas  y  de  gran capacidad de almacenamiento, aunque lentas. 

#### Medios de almacenamiento óptico 

Los  más  comunes  son  CD  (Compact  Disk),  DVD  (Digital  Versatile  Disk)  y  Blu-ray.  Emplean diferente  tecnología  láser  para  grabar  o  leer  en  la  superficie  de  los  discos,  almacenando información en forma de crestas y surcos. La capacidad también es un aspecto importante entre ellos, ya que cada uno puede tener: 

- CD: hasta 700 MB. 
- DVD: hasta 17 GB. 
- Blu-ray: hasta 128 GB. 

Para leer, grabar o regrabar información necesitan unidades ópticas hábiles a una determinada velocidad, representada por “X”. 

Están en decadencia debido al auge del almacenamiento en la nube, discos duros externos (muy compactos y portables) y almacenamiento Flash. 

Los medios de almacenamiento secundario más empleados en la pequeña y median empresa, son los medios Flash y discos duros mecánicos. Las ventajas de cualquier dispositivo Flash son: menos consumo de energía, más ligeros, gran velocidad en operaciones de lectura y escritura, y más resistentes, al no incorporar partes móviles. 

Los dispositivos magnéticos son todavía una buena solución desde el punto de vista económico y de backup. 

### Fuente de alimentación 

La  alimentación  eléctrica  en  cualquier  sistema  informático  es  fundamental,  ya  que  de  él dependen todos los componentes del equipo.  

La fuente de alimentación es la encargada de proporcionar energía a la placa base, así como a todos los elementos que la rodean. Tiene tres objetivos principalmente: 

1. Suministrar energía a todos los componentes. 
1. Actuar de barrera o protección ante alteraciones (ruidos o picos) de la red eléctrica externa. 
1. Facilitar la extracción del flujo de aire caliente del sistema en equipos de sobremesa. 

La fuente de alimentación transforma la tensión de entrada de 230 voltios a valores inferiores, rectifica la corriente alterna en continua, filtra la señal y la estabiliza.

En fuentes de alimentación para placas ATX, los voltajes de salida son de 3,3 V, 5 V, 12 V y -12 V. Además, según el componente a alimentar nos encontramos con distintos conectores y cables de alimentación.

![](019.png)

### Periféricos

Son los dispositivos a través de los cuales los usuarios interactúan con el sistema informático. Se clasifican en: 

1. ***Dispositivos de entrada:*** permiten introducir información al sistema (ratón, teclado, micrófono…). 
1. ***Dispositivos de salida:*** únicamente ofrecen al usuario información (pantalla, impresora, altavoces…). 
1. ***Dispositivos de entrada y salida:*** ambas tareas. (Pantalla táctil). Podemos encontrar: 
1. ***Dispositivos  de  almacenamiento:***  permiten  almacenara  y  recuperar información (discos duros, DVD…). 
1. ***Comunicación:*** permiten la comunicación entre ordenadores o elementos de interconexión de un sistema en red (tarjeta Ethernet o Wi-Fi). 

Los **adaptadores** permiten a los periféricos ser utilizados empleando otra conexión diferente a la  utilizada  por  el  sistema  informático  al  que  se  van  a  asociar.  Prácticamente  todos  los conectores disponen de una gran variedad de adaptadores (por ejemplo, PS/2 a USB, USB-A a USB-C, HDMI/VGA a Displayport…)

## Normas de seguridad y prevención de riesgos laborales 

Debemos adoptar unas recomendaciones ergonómicas y de seguridad básicas de cara a prevenir o minimizar cualquier riesgo laboral. 

En España, la Ley 31/1995, de prevención de riesgos laborales, establece la seguridad para el trabajador cuando realiza sus actividades laborales. Esta ley señala que “los trabajadores tienen derecho a una protección eficaz en materia de seguridad y salud en el trabajo”. 

Tanto el empresario como el trabajador tienen una serie de derechos y obligaciones en materia de riesgos laborales. Algunos de los derechos son: información a los trabajadores, evaluación de riesgos en el puesto de trabajo, formación o planes de emergencia ante riesgos graves. Para prevenir los riesgos laborales se debe: 

1. Adoptar un plan de prevención de riesgos laborales. 
1. Evaluar los riesgos. 
1. Planificar y ejecutar la actividad preventiva. 

En nuestro caso, destacamos las siguientes normas de seguridad y prevención con respecto a los equipos con pantallas de visualización: 

1) Pantalla: 
   1. Los caracteres deben estar bien definidos y configurados de forma clara. 
   1. El usuario deberá poder ajustar fácilmente la luminosidad y el contraste entre los caracteres y el fondo de la pantalla, y adaptarlos fácilmente al entorno. 
   1. La pantalla deberá ser orientable e inclinable a voluntad, con facilidad para adaptarse a las necesidades del usuario. 
   1. La pantalla no deberá tener reflejos ni reverberaciones que puedan molestar. 
1) Teclado: 
   1. El teclado deberá ser inclinable e independiente de la pantalla para permitir adoptar una postura cómoda que no provoque cansancio en los brazos o las manos. 
   1. Tendrá que haber espacio suficiente delante del teclado para que el usuario pueda apoyar los brazos y las manos. 
1) Mesa o superficie de trabajo: 
   1. Debe tener dimensiones suficientes y permitir una colocación flexible de la pantalla, teclado, los documentos y el material accesorio. 
   1. El espacio debe ser suficiente para permitir a los usuarios una posición cómoda. 
1) Asiento de trabajo: 
   1. Deberá ser estable, regulable en altura, proporcionando al usuario libertad de movimiento y procurándole una postura confortable. 
1) Entorno: 

1. Debe existir un espacio de dimensiones suficiente para adoptar cambios de postura y movimientos de trabajo. 
1. La iluminación debe ser adecuada, evitando deslumbramientos y reflejos. 
1. El ruido no debe perturbar la atención del trabajador. 
1. Las condiciones atmosféricas de temperatura y humedad deben ser adecuada para el desarrollo del trabajo. 

![](020.png)

Cuando nos sentamos para trabajar con un ordenador, es conveniente tomar una postura adecuada: regular la altura del asiento, la mesa, el apoyo lumbar y el respaldo, apoyar el antebrazo cuando escribimos con el teclado o manejamos el ratón, regular la inclinación y altura de la pantalla… 

Además, al utilizar los dispositivos eléctricos, debemos: 

1. Leer los manuales de instrucciones de uso de todos los componentes eléctricos. 
1. Mantener los componentes eléctricos en buen estado. 
1. Desconectar los componentes de la red eléctrica cuando no vayan a ser utilizados. 
1. Disponer de una instalación eléctrica adecuada para nuestros sistemas y que permita evitar accidentes ante corrientes excesivas o derivaciones. 
1. Manejar  correctamente  y  con  los  medios  necesarios  los  dispositivos  sensitivos  a descargas eléctricas. 
1. Evitar manipular los componentes con las manos mojadas o húmedas. 
1. Cuando  se  acceda  al  interior  de  los  dispositivos  eléctricos,  estos  deben  estar desconectados de la red eléctrica. 
1. No desplazar equipos no portables cuando están en funcionamiento. 

**RECOMENDACIONES:** 

- El teclado ha de estar situado como mínimo a 10 cm de distancia desde el borde de la mesa. 
- El ratón debe estar cerca del teclado. 
- La pantalla debe estar a una distancia mínima de 40 cm. 
- La silla debe permitir tener un apoyo completo lumbar y ser regulable. 
- Mantener una postura erguida, con las rodillas a la altura de la pelvis y los brazos apoyados. 



## Secuencia de Montaje 

### Apertura de la caja 

Los chasis de las computadoras se producen en diversos factores de forma. Los factores de forma hacen referencia al **tamaño** y a la **forma** del chasis. 

Existen diferentes métodos para abrir los chasis. Para conocer cómo abrir un chasis específico, consulte el manual del usuario o el sitio Web del fabricante. La mayoría de los chasis se abren de una de las siguientes formas: 

- Se puede retirar la carcasa del chasis en una sola pieza. 
- Se pueden retirar los paneles superiores y laterales del chasis. 
- Es posible que deba retirar la parte superior del chasis antes de poder retirar las tapas laterales. 

### Instalación de la fuente 

Es posible que un técnico deba reemplazar o instalar la fuente de energía. La mayoría de las fuentes de energía se pueden colocar de una única forma en el chasis de la computadora. En general, hay tres o cuatro tornillos que sujetan la fuente de energía al chasis.  Las  fuentes  de  energía  tienen  ventiladores  que  pueden  vibrar  y  aflojar  los tornillos que no están asegurados. Al instalar una fuente de energía, asegúrese de que se utilicen todos los tornillos y de que estén ajustados correctamente. 

Éstos son los pasos que se deben seguir para la instalación de la fuente de energía: 

- Insertar la fuente de energía en el chasis. 
- Alinear los orificios de la fuente de energía con los del chasis.  
- Asegurar la fuente de energía en el chasis con los tornillos adecuados. 

### Instalación de la Placa base 

Lo  primero  es  instalar  componentes  en  la  motherboard  y  después  instalar  la motherboard en el chasis de la computadora. 

1. Instalación de una CPU y ensamblado de un disipador de calor o ventilador. 

La CPU y el disipador de calor o ventilador se pueden instalar en la placa base antes de colocarla en el chasis de la computadora. 

La CPU y la placa son sensibles a las descargas electrostáticas. Al manipular una CPU y una placa, asegúrese de colocarlas sobre una alfombrilla antiestática con descarga a tierra. Al trabajar con estos componentes, debe usar una pulsera antiestática. 

**PRECAUCIÓN**:  Al  manipular una  CPU,  no  toque  los  contactos  de  la  CPU  en ningún momento.  ![](021.png)

La CPU se sujeta al socket de la motherboard con un  dispositivo de sujeción. En la actualidad, los sockets de  la  CPU  son  de  tipo  **LGA**  (Land  Grid  Array,  los  más  modernos) en los que el propio socket incluye los pines  en vez de hacerlo la pastilla del microprocesador.   

Se debe colocar pasta térmica en la superficie del micro que irá en contacto con el disipador para facilitar su función.  

Cuando instale una CPU usada, limpie la CPU y la base del disipador de calor con **alcohol isopropílico**. De esta forma, eliminará todos los restos del compuesto térmico anterior. Una  vez  que  las  superficies  estén  listas  para  la  aplicación  de  una  nueva  capa  de compuesto  térmico,  siga  las  instrucciones  del  fabricante  sobre  la  aplicación  del compuesto térmico. 

El  disipador  de  calor  remueve  el  calor de  la  CPU.  El  ventilador  mueve  el  calor  del disipador hacia el exterior. 

Siga  estas  instrucciones  para  instalar  la  CPU  y  ensamblar  el  disipador  de  calor  o ventilador: 

1) Alinee la CPU de modo que el indicador de la Conexión 1 coincida con el Pin 1 del socket de la CPU. De esta forma, garantizará que las muescas de orientación de la CPU estén alineadas con las flechas de orientación del socket de la CPU. 
1) Conecte suavemente la CPU en el socket. 
1) Cierre la placa de carga de la CPU y fíjela. Para ello, cierre la palanca de carga y muévala por debajo de la pestaña de retención de la palanca. 
1) Aplique una pequeña cantidad de compuesto térmico a la CPU y distribúyalo de forma pareja. Siga las instrucciones de aplicación del fabricante.  
1) Alinee los dispositivos de retención del ensamblado del disipador de calor o ventilador con los orificios de la placa base. 
1) Coloque el ensamblaje del disipador de calor o ventilador en el socket de la CPU. Tenga cuidado para no apretar los cables del ventilador de la CPU. 
1) Ajuste  los dispositivos  de  retención  del  ensamblaje del  disipador  de  calor o ventilador para mantenerlo en su lugar. 
2. Instalación de la memoria 

Colocar  la  memoria  RAM  en  la  motherboard  antes  de  colocarla  en  el  chasis  de  la computadora.  Antes  de  instalar  un  módulo  de  memoria,  consulte  el  manual  de  la motherboard o el sitio Web del fabricante para asegurarse de que la memoria RAM sea compatible.  

Para instalar la memoria RAM, siga estos pasos: 

1) Alinee las muescas del módulo de  memoria RAM con las flechas de la  ranura y presione la memoria RAM  hasta  que  las  pestañas  laterales  estén en su lugar.   ![](022.png)
2) Asegúrese  de  que  las  pestañas  laterales traben en el módulo RAM.  Haga  una  inspección  visual  para  determinar  la  existencia  de  contactos expuestos.   
3) Para  montar  la  motherboard  y  evitar que  entre en  contacto  con las  piezas  metálicas  del  chasis,  se  utilizan soportes  de  plástico  o metal.  Solamente  se deben  colocar  los  soportes  que coincidan  con  los  orificios  de  la  motherboard.  La  instalación  de  soportes adicionales puede impedir que la motherboard quede colocada correctamente en el chasis. 
3. Instalación de la motherboard Siga los siguientes pasos: 
1) Instale los soportes en el chasis de la computadora.  
1) Alinee los conectores de E/S de la parte trasera de la motherboard con las aberturas de la parte trasera del chasis.  
1) Alinee los orificios para tornillos de la motherboard con los soportes.  
1) Coloque todos los tornillos de la motherboard. 
1) Ajuste todos los tornillos de la motherboard. 
4. Instalación de Unidades externas 

Las unidades que se instalan en los compartimientos internos se denominan unidades internas. Una unidad de disco duro (HDD, hard disk drive) constituye un ejemplo de una unidad interna. 

### Instalación de un Disco Duro

1) Coloque la HDD de modo que quede alineada con el compartimiento de la unidad de 3,5 in. 
1) Inserte la HDD en el compartimiento de la unidad de modo que los orificios para tornillos de la unidad coincidan con los del chasis. 
1) Asegure la HDD en el chasis con los tornillos adecuados. 

Una unidad óptica es un dispositivo de almacenamiento que lee y escribe información en CD y DVD. El conector de alimentación **Molex** suministra energía a la unidad óptica desde la fuente de energía. El cable **PATA** conecta la unidad óptica a la motherboard. 

- Para instalar la unidad óptica, siga estos pasos:
  - Coloque la unidad óptica de modo que quede alineada con el compartimiento de la unidad de 5,25 in. 
  - Inserte la unidad óptica en el compartimiento de la unidad de modo que los orificios para tornillos de la unidad óptica coincidan con los del chasis. 
  - Asegure la unidad óptica en el chasis con los tornillos adecuados. 

### Instalación de Tarjetas 

#### Tarjeta de red

####   ![](026.png)

La tarjeta de red o NIC (Network Interface Controller) permite que la computadora se conecte a  una red. Utiliza ranuras de expansión PCI y PCIe  en la motherboard. 

Para instalar la NIC, siga los siguientes pasos:

- Alinee la NIC con la ranura de expansión  correspondiente de la motherboard.
- Presione suavemente la NIC hasta que la tarjeta quede colocada correctamente.
- Asegure la consola de montaje de la NIC para PC en el chasis con el tornillo adecuado. 

#### Tarjeta de video

Una tarjeta adaptadora de vídeo es la interfaz entre una computadora y un monitor. Una  tarjeta  adaptadora  de  vídeo  actualizada  proporciona una mayor  resolución  de gráficos para juegos y programas de presentación. Las tarjetas adaptadoras de vídeo utilizan ranuras de expansión PCI, AGP y PCIe en la motherboard.

Para instalar la tarjeta adaptadora de vídeo, siga estos pasos:

1) Alinee  la  tarjeta  adaptadora  de  vídeo  con  la  ranura  de  expansión correspondiente de la motherboard. 
1) Presione suavemente la tarjeta adaptadora de vídeo hasta que la tarjeta quede colocada correctamente.
1) Asegure la consola de montaje para PC de la tarjeta adaptadora de vídeo en el chasis con el tornillo adecuado. 

### Cables internos: conexiones de alimentación de la motherboard. 

Al  igual  que  otros  componentes,  las  motherboards  necesitan  electricidad  para funcionar.  El  conector  de  alimentación  de  tecnología  avanzada  extendida  (ATX, Advanced Technology Extended) tiene 20 o 24 pines. Además, la fuente de energía puede tener un conector de alimentación auxiliar (AUX) de 4 o 6 pines que se conecta a la motherboard.

Para instalar el cable de alimentación de la motherboard, siga estos pasos:

- Alinee el conector de alimentación ATX de 20 pines con el socket de la motherboard.  Presione suavemente el conector hasta que el clip esté en su lugar. 
- Alinee el conector de alimentación AUX de 4 pines con el socket de la motherboard.  Presione suavemente el conector hasta que el clip esté en su lugar.

Para instalar el cable de alimentación del micro

- Alinee el conector de alimentación de 4 pines con el socket.  Presione suavemente el conector hasta que el clip esté en su lugar.

Para instalar el cable de alimentación del ventilador del micro.

- Alinee el conector de alimentación del ventilador (normalmente de 3 pines).  Insértelo en su lugar.

### Conectores de alimentación SATA

Los conectores de alimentación SATA utilizan un conector de 15 pines. Los conectores de alimentación SATA se utilizan para conectarse a discos duros, unidades ópticas o cualquier dispositivo que tenga un socket de alimentación SATA.

### Conectores de alimentación Molex

Los discos duros y las unidades ópticas que no tienen sockets de alimentación SATA utilizan conector de alimentación Molex.

> PRECAUCIÓN: No utilice un conector Molex y un conector de alimentación SATA en la misma unidad al mismo tiempo.

### Conectores de alimentación Berg

Tiene 4 pines y suministran electricidad a las unidades de disquete.

Instalación de conectores de alimentación

- Conecte el conector de alimentación SATA a la HDD.

- Conecte el conector de alimentación Molex a la unidad óptica.  Conecte el conector de alimentación Berg de 4 pines a la FDD.

- Conecte los cables adicionales del chasis a los conectores correcpondientes, según las instrucciones del manual de la motherboard (ventiladores de caja, alimentación de tarjeta gráfica...).

### Cables datos 

#### Cables de datos PATA (IDE) 

A menudo, el cable PATA se denomina cable plano debido a que es ancho y plano. Además, el cable PATA puede tener 40 u 80 conductores. Generalmente, un cable PATA tiene tres conectores de 40 pines. En el extremo del cable, hay un conector que se conecta a la motherboard. Los otros dos conectores se conectan a las unidades. Si se instalan varios discos duros, la unidad principal se conectará al conector del extremo del cable. La unidad secundaria se conectará al conector intermedio. 

El revestimiento del cable de datos indica el pin 1. Conecte el cable PATA a la unidad con el indicador del pin 1 del cable alineado con el indicador del pin 1 del conector de la unidad. El indicador del pin 1 del conector de la unidad generalmente se encuentra más cerca del conector de alimentación de la unidad. 

#### Cables de datos SATA 

El cable de datos SATA cuenta con un conector de 7 pines. Un extremo del cable se conecta a la motherboard. El otro extremo se conecta a cualquier unidad que cuente con un conector de datos SATA. 

#### Cables de datos de unidad de disquete 

El cable de datos de unidad de disquete cuenta con un conector de 34 pines. Un cable de unidad de disquete generalmente cuenta con tres conectores de 34 pines. En el extremo del cable, hay un conector que se conecta a la motherboard. Los otros dos conectores se conectan a las unidades. Si se instalan varias unidades de disquete, la unidad A: se conectará al conector del extremo. La unidad B se conectará al conector intermedio. 

> NOTA: Si el pin 1 del cable de datos de la unidad de disquete no está alineado con el pin 1 del conector de la unidad, la unidad de disquete no funcionará. La falta de alineación no  dañará  la  unidad.  Sin  embargo,  la  luz  de  actividad  de  la  unidad  se  encenderá continuamente.  Para  solucionar  este  problema,  apague  la  computadora  y  vuelva  a conectar el cable de datos para que el pin 1 del cable y el pin 1 del conector estén alineados. Reinicie la computadora. 

### Cables del Panel frontal 

Los cables que provienen del frontal de la caja deben conectarse en su correspondiente conector de la placa base. Estos cables suelen venir separados y cada uno de ellos deberá conectarse en los pines adecuados. 

El  manual  de  la  placa  base  proporciona  información  sobre  la  posición  correcta  de colocación. 

[[Preguntas_Moodle]]
