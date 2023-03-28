# ¿Qué es Docker y para qué se utiliza? [[1](http://apuntes.ucr.ac.cr/index.php/Docker,_aplicaciones_en_cualquier_parte)]
 
 **Docker** es una herramienta que puede empaquetar una aplicación y sus dependencias en un contenedor virtual que se puede ejecutar en cualquier servidor Linux. Es muy flexible y portable, de manera que se puede desplegar en infraestructura física, nube privada, nube pública, etc. Actualmente es soportado también por sistemas como Windows y macOS.

[![](http://apuntes.ucr.ac.cr/images/1/19/Virtual-machine.png)](http://apuntes.ucr.ac.cr/index.php/Archivo:Virtual-machine.png)

Arquitectura de una máquina virtual

[![](http://apuntes.ucr.ac.cr/images/d/d3/Docker-container.png)](http://apuntes.ucr.ac.cr/index.php/Archivo:Docker-container.png)

Arquitectura de un contenedor Docker, donde el kernel del anfitrión es compartido

Es virtualización a nivel de sistema operativo que, a diferencia de otros tipos como emulación (VirtualBox), paravirtualización (Xen), o virtualización completa (VMWare, KVM), comparten el kernel o núcleo del anfitrión lo que lo hace más ligero.