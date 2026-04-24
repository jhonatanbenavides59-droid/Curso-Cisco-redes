# Resumen Capitulos Conceptos básicos de redes 2026-1
## Jhonatan Steevens Benavides Alfonso, jsbenavidez@ucompensar.edu.co 

# Capitulo 1
## Conmutación en un mundo conectado
Se repasará de manera sencilla los conceptos básicos de cómo funciona el internet donde para la mayoría del mundo se trata solo de tener navegación en algún dispositivo final, pero no cae en cuenta de toda la infraestructura y configuraciones que se hacen para poder tener acceso a algo muy usado hoy en día como una página web, mostrando los diferente tipos de red que se pueden crear, un ejemplo es entornos domésticos donde se pueden usar distintos elementos como cámaras de seguridad, televisores, consolas entre otros usando conexiones a internet para su interconexión.
De igual forma vemos una parte fundamental de la transmisión de datos ya que para los computadores la lengua nativa son 0 (falso) y 1(verdadero) llamado Bit el principal sistema que se usa para que se entiendan entre los diferentes dispositivos que hay en una red. Se hace un enfoque en los principales métodos de transmisión de datos, señales eléctricas que usa pulsos de electricidad, señales ópticas que usa pulsos de luz, señales inalámbricas que usan ondas de radio, donde se validan las diferencias de cada método, tocando un tema muy importante como lo es el ancho de banda (capacidad de un medio para transmitir datos de un punto a otro) y sus diferentes formas de medición como lo son Bps, Kbps, Mbps, Gbps, Tbps, dato con gran relevancia que se usa para el envío y recepción de toda la información que es necesaria para que funcione el internet


# Capitulo 2
## Componentes, tipos y conexiones de red
Se habla del término cliente servidor que hace parte fundamental de una red, ya que el cliente puede ser un equipo que está necesitando un servicio como correo electrónico, acceso a un archivo entre otros, el servidor es quien ofrece este servicio usando software dependiendo de la solicitud, se tiene varias alternativas para estos casos ya que un cliente puede servidor al mismo tiempo, pero se debe analizar cada cas para tener la claridad del uso que se le dará ala red para que el rendimiento del servicio sea el esperado, existen varias formas de interactuar entre cliente y servidor la mas sencilla es llamada entre pares o la mas recomendada un cliente que solicite servicios a varios servidores, para esto es necesario tener claro que la red esta divida en niveles de dispositivos en tres secciones como los son dispositivos finales(computadores, celulares, impresoras), dispositivos intermedios (switch,router, firewall) , medios de red (lan, wan, inalámbrico), el  siguiente paso es saber cómo realizar la conexión a internet de la red que se tenga para estos casos existen diferentes formas de realizarlo, por medio de un ISP quien será nuestro proveedor principal quien ya tiene las interconexiones necesarias entre otro ISP formando una gran red, con esto afinado se pasa a la parte de conexiones que se usaran para los usuarios finales, ya sea usando cable, red inalámbrica, red móvil o red satelital. 

# Capitulo tres
## Capa de aplicación
Es la capa superior (capa 7 del modelo OSI) y permite que las aplicaciones de usuario se comuniquen a través de la red.
Define:
•	Formato de los datos
•	Tipos de mensajes
•	Reglas de comunicación entre dispositivos

- Relación OSI vs TCP/IP
•	Los protocolos TCP/IP no separan claramente las capas de sesión y presentación.
•	Estas funciones suelen estar integradas en la capa de aplicación.

- Capa de presentación
Se encarga de:
•	Convertir y codificar datos
•	Comprimir información
•	Cifrar y descifrar datos

- Capa de sesión
Su función es:
•	Establecer, mantener y finalizar conexiones
•	Controlar el diálogo entre aplicaciones
•	Recuperar sesiones interrumpidas

- Protocolos principales
•	DNS: Traduce nombres a IP
•	HTTP / HTTPS: Transferencia web (HTTPS es seguro)
•	SMTP: Envío de correos
•	POP3 / IMAP: Recepción de correos
•	FTP: Transferencia de archivos
•	Telnet / SSH: Acceso remoto (SSH es seguro)

- Servidores de red
•	Responden a solicitudes de clientes
•	Ejecutan procesos llamados daemons
•	Ejemplos: DNS, web, correo, FTP, DHCP

- Aplicaciones vs servicios
•	Aplicaciones: usadas por el usuario (navegador, email)
•	Servicios: procesos que permiten la comunicación
 Las aplicaciones crean los mensajes; los protocolos definen cómo se envían

- Modelo cliente-servidor
•	Cliente solicita
•	Servidor responde
•	Puede haber autenticación
•	Tipos de comunicación:
o	Descarga
o	Subida

- Redes P2P
•	No hay servidor central
•	Cada equipo puede ser cliente y servidor
•	Ejemplo: Gnutella

- Puertos
Permiten dirigir datos a la aplicación correcta:
•	DNS → 53
•	HTTP → 80
•	HTTPS → 443
•	SMTP → 25
•	FTP → 20/21
•	Telnet → 23
•	DHCP → 67

- DNS
•	Convierte nombres de dominio a IP
•	Estructura jerárquica
•	Usa registros (A, NS, CNAME, MX)
•	Utiliza caché para mayor eficiencia

- Servicios web y correo
•	HTTP usa métodos como GET, POST, PUT
•	HTTPS añade seguridad (cifrado)
•	Correo electrónico:
o	MUA: cliente
o	MTA: transporte
o	MDA: entrega

# Capitulo cuatro

1. Función de la capa de transporte
La capa de transporte (capa 4 del modelo OSI) se encarga de la comunicación extremo a extremo entre aplicaciones que se ejecutan en dispositivos de origen y destino.
Funciones principales:

Segmentar datos para su transmisión
Controlar la comunicación entre dispositivos finales
Garantizar la entrega de datos cuando el protocolo lo requiere
Multiplexar aplicaciones mediante el uso de números de puerto

 2. Segmentación y reensamblaje

Los datos grandes se dividen en segmentos antes de enviarse
Cada segmento viaja de forma independiente por la red
En el dispositivo de destino, los segmentos se reensamblan en el orden correcto

✅ Esto mejora la eficiencia y confiabilidad de la transmisión.

 3. Control de la comunicación
La capa de transporte puede:

Establecer o no una conexión
Asegurar la entrega confiable de los datos
Controlar la velocidad de envío para evitar saturar al receptor


4. Protocolos principales de la capa de transporte
- TCP (Transmission Control Protocol)

Orientado a conexión
Confiable
Usa confirmaciones (ACK)
Reenvía datos perdidos
Controla flujo y congestión
- Usado en:

HTTP / HTTPS
FTP
Correo electrónico (SMTP, POP3, IMAP)

- UDP (User Datagram Protocol)

No orientado a conexión
No garantiza entrega
Más rápido y ligero
No utiliza confirmaciones ni control de errores

- Usado en:

Streaming de audio y video
Juegos en línea
DNS

5. Diferencias clave entre TCP y UDP

<img width="633" height="166" alt="image" src="https://github.com/user-attachments/assets/88351e84-ab75-43dc-9ec4-85824d01ff86" />


6. Puertos
Los puertos permiten identificar qué aplicación debe recibir los datos dentro de un dispositivo.
Funciones:

Permiten múltiples comunicaciones simultáneas
Identifican procesos de origen y destino

Tipos de puertos:

Bien conocidos (0–1023) → HTTP (80), HTTPS (443)
Registrados (1024–49151)
Dinámicos o efímeros (49152–65535)


7. Multiplexación y demultiplexación

Multiplexación: el envío simultáneo de datos de varias aplicaciones
Demultiplexación: la recepción y entrega correcta de los datos a la aplicación correspondiente


8. Comunicación confiable con TCP
TCP garantiza la entrega confiable mediante:

Números de secuencia
Confirmaciones (ACK)
Reenvío de segmentos perdidos
Control de flujo mediante ventana deslizante


9. Establecimiento de conexión (Three-Way Handshake)
TCP establece una conexión usando tres pasos:

Cliente → SYN
Servidor → SYN-ACK
Cliente → ACK

Con esto, la conexión queda establecida.

10. Finalización de la conexión

Se utilizan mensajes FIN y ACK
Permite cerrar la sesión de forma ordenada
Libera recursos del sistema y de la red

11. Control de flujo y congestión

Evita que el emisor envíe datos más rápido de lo que el receptor puede procesar
Ajusta dinámicamente la velocidad según las condiciones de la red
Reduce pérdidas y congestión

# Capítulo 5
## Principios de comunicación

En este capítulo se explican las reglas que permiten la comunicación entre dispositivos, conocidas como protocolos. Se introduce el concepto de comunicación estructurada.
Se analiza cómo los datos se encapsulan en unidades llamadas segmentos, paquetes y tramas, dependiendo de la capa del modelo OSI.
El capítulo también explica la sincronización, codificación y control de flujo en la transmisión de datos.
Se introduce el concepto de direccionamiento lógico y físico, necesario para identificar dispositivos en la red.
Además, se estudian los modelos de referencia como OSI y TCP/IP, que organizan las funciones de red en capas.
Finalmente, se destaca la importancia de los protocolos para garantizar comunicación confiable y eficiente

# Capítulo 6
## Medios de red

Este capítulo describe los diferentes medios por los que se transmiten los datos. Se incluyen cables de cobre, fibra óptica y medios inalámbricos.
Se analizan las características físicas de cada medio, como velocidad, distancia máxima y susceptibilidad a interferencias.
El capítulo también explica cómo se codifican las señales para transmitir información.
Se comparan ventajas y desventajas de cada medio, destacando la fibra óptica por su alta capacidad y baja pérdida.
Además, se introducen conceptos como latencia y ruido, que afectan la calidad de la transmisión.
Finalmente, se enfatiza la correcta selección del medio según la aplicación.

# Capítulo 7
## La capa de acceso

Este capítulo se enfoca en la capa de acceso a la red, donde los dispositivos se conectan directamente.
Se explica el funcionamiento de switches, que utilizan direcciones MAC para enviar datos dentro de una red local.
El capítulo introduce el concepto de conmutación y aprendizaje de direcciones MAC.
También se abordan problemas como colisiones y dominios de broadcast.
Se explica el uso de VLANs para segmentar redes y mejorar seguridad y rendimiento.
Finalmente, se destaca la importancia de esta capa en la eficiencia de la red

# Capítulo 8
## El protocolo de Internet (IP)

Este capítulo introduce el Protocolo de Internet (IP) como el mecanismo principal para el direccionamiento y envío de paquetes en redes. IP permite identificar de forma única a cada dispositivo conectado, facilitando la comunicación entre redes diferentes.
Se explica que IP es un protocolo no orientado a conexión, lo que significa que no garantiza la entrega de los paquetes. En lugar de ello, se basa en el principio de “mejor esfuerzo”, donde los datos pueden perderse, duplicarse o llegar fuera de orden.
El capítulo también aborda la estructura básica de un paquete IP, incluyendo encabezados que contienen información como dirección de origen, destino y tiempo de vida (TTL). Estos campos son fundamentales para el enrutamiento.
Se introduce el concepto de fragmentación, que ocurre cuando un paquete es demasiado grande para un medio de transmisión y debe dividirse en partes más pequeñas.
Además, se explica la diferencia entre IPv4 e IPv6 a nivel conceptual, preparando al estudiante para los capítulos siguientes.
Finalmente, se destaca la importancia de IP como base de internet, ya que permite la interconexión de redes heterogéneas a nivel global.

# Capítulo 9
## Direccionamiento IPv4

Este capítulo profundiza en el esquema de direccionamiento IPv4, basado en direcciones de 32 bits representadas en formato decimal punteado.
Se explica la estructura de una dirección IPv4, dividida en parte de red y parte de host, lo que permite identificar tanto la red como el dispositivo.
El capítulo introduce las clases de direcciones (A, B, C), aunque también se menciona el uso moderno de CIDR para una asignación más eficiente.
Se analizan conceptos como máscaras de subred, que permiten segmentar redes en subredes más pequeñas, mejorando la organización y seguridad.
Además, se estudian direcciones especiales como la dirección de broadcast y la dirección de red, fundamentales para la comunicación en redes locales.
Finalmente, se destaca la limitación del espacio de direcciones IPv4 y la necesidad de técnicas como NAT para extender su uso.

# Capítulo 10
## Direccionamiento IPv6

Este capítulo presenta IPv6 como la solución al agotamiento de direcciones IPv4, utilizando direcciones de 128 bits.
Se explica el formato hexadecimal de las direcciones IPv6 y su representación abreviada, lo que facilita su uso.
El capítulo también introduce los tipos de direcciones IPv6, como unicast, multicast y anycast, cada uno con funciones específicas.
Se analiza la autoconfiguración sin estado (SLAAC), que permite a los dispositivos generar automáticamente su dirección IP.
Además, se destacan mejoras en IPv6 como mayor seguridad, eficiencia en el enrutamiento y eliminación de NAT.
Finalmente, se enfatiza la transición gradual de IPv4 a IPv6 en redes modernas.

# Capítulo 11
## Direccionamiento dinámico con DHCP

En este capítulo se estudia el Protocolo de Configuración Dinámica de Host (DHCP), que permite asignar direcciones IP automáticamente.
Se describe el proceso de comunicación DHCP en cuatro pasos: Discover, Offer, Request y Acknowledge (DORA).
El capítulo explica cómo DHCP simplifica la administración de redes, evitando configuraciones manuales.
También se introducen conceptos como tiempo de concesión (lease) y reservas de direcciones.
Se analiza el papel del servidor DHCP en redes empresariales y domésticas.
Finalmente, se destaca su importancia para la escalabilidad y eficiencia en la gestión de direcciones IP.

# Capítulo 12
## Puertas de enlace a otras redes

Este capítulo explica el concepto de puerta de enlace o gateway, que permite la comunicación entre redes diferentes.
Se describe cómo los dispositivos envían tráfico fuera de su red local a través de un router.
El capítulo analiza el proceso de decisión que realiza un host para determinar si el destino está en su red o en otra.
También se introduce la tabla de enrutamiento básica en los dispositivos.
Se explica la importancia de la puerta de enlace predeterminada en redes domésticas y empresariales.
Finalmente, se destaca su papel en el acceso a internet.

# Capitulo 13 
## Resolución de dirección

Este capítulo aborda el protocolo ARP (Address Resolution Protocol), utilizado para mapear direcciones IP a direcciones MAC.
Se explica cómo un dispositivo consulta en la red para obtener la dirección física correspondiente a una IP.
El capítulo describe el funcionamiento de la tabla ARP y su almacenamiento temporal.
También se analizan problemas de seguridad como el ARP spoofing.
Se introduce el equivalente en IPv6, conocido como Neighbor Discovery Protocol (NDP).
Finalmente, se destaca la importancia de la resolución de direcciones para la comunicación en redes locales.

# Capitulo 14 
## Enrutamiento entre redes

En este capítulo se estudia el proceso de enrutamiento, mediante el cual los routers determinan la mejor ruta para enviar paquetes.
Se explica la diferencia entre enrutamiento estático y dinámico.
El capítulo introduce conceptos como métricas, rutas y tablas de enrutamiento.
También se analizan protocolos de enrutamiento básicos.
Se describe el proceso de reenvío de paquetes en un router.
Finalmente, se destaca la importancia del enrutamiento en la conectividad global.

# Caputilo 15 
## Capa de transporte

Este capítulo se centra en la capa de transporte del modelo OSI, responsable de la entrega de datos entre aplicaciones.
Se estudian los protocolos TCP y UDP, destacando sus diferencias en confiabilidad y velocidad.
TCP proporciona comunicación confiable mediante control de errores y confirmaciones.
UDP, en cambio, es más rápido pero no garantiza la entrega de datos.
El capítulo también introduce el concepto de puertos, que permiten identificar aplicaciones.
Finalmente, se destaca la importancia de elegir el protocolo adecuado según la aplicación.

# Caputlo 16 
## Servicios de la capa de aplicación

Este capítulo describe los servicios que utilizan los usuarios finales, como web, correo electrónico y resolución de nombres.
Se explican protocolos como HTTP, HTTPS, DNS y SMTP.
El capítulo analiza cómo estos servicios funcionan sobre la red.
También se estudia la interacción entre cliente y servidor.
Se destaca la importancia de la seguridad en servicios como HTTPS.
Finalmente, se enfatiza el papel de esta capa en la experiencia del usuario.

# Capitulo 17
## Utilidades de prueba de red

Este capítulo presenta herramientas utilizadas para diagnosticar y solucionar problemas de red.
Se explican comandos como ping, traceroute e ipconfig.
El capítulo analiza cómo estas herramientas ayudan a identificar fallos de conectividad.
También se introduce el uso de estadísticas de red.
Se destaca la importancia del monitoreo continuo.
Finalmente, se enfatiza el papel de estas herramientas en la administración de redes






