# Redes
En Docker, las redes son una forma de **conectar contenedores y permitir que se comuniquen entre sí** y con otros servicios en la red. Las redes de Docker se utilizan para facilitar la comunicación entre contenedores y para aislar los contenedores de otras redes.
Docker proporciona varios tipos de redes, que se utilizan para diferentes propósitos:
1. **Bridge network (red puente)**: Es la red predeterminada en Docker. Cada contenedor se conecta a una red puente virtual, que se encuentra en el host. Los contenedores en la misma red puente pueden comunicarse entre sí mediante sus nombres de host.
2. **Host network (red de host)**: En esta red, los contenedores se conectan directamente a la red del host, en lugar de a una red virtual. Esto permite que los contenedores tengan acceso directo a los recursos de red del host, pero también puede presentar problemas de seguridad.
3. **Overlay network (red de superposición)**: Esta red se utiliza para conectar contenedores que se ejecutan en diferentes hosts. Los contenedores en la misma red de superposición pueden comunicarse entre sí como si estuvieran en la misma red local.
4. **Macvlan network (red de Macvlan)**: Esta red se utiliza para conectar contenedores directamente a una interfaz de red física del host. Esto permite que los contenedores tengan direcciones IP únicas y se comuniquen directamente con otros dispositivos en la red.
Además de estos tipos de redes, Docker también permite crear redes personalizadas para satisfacer las necesidades específicas de una aplicación o servicio.
