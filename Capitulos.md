# Resumen Capitulos Conceptos básicos de redes 2026-1
## Jhonatan Steevens Benavides Alfonso, jsbenavidez@ucompensar.edu.co 

# - Capitulo uno 
## Conmutación en un mundo conectado
Se repasará de manera sencilla los conceptos básicos de cómo funciona el internet donde para la mayoría del mundo se trata solo de tener navegación en algún dispositivo final, pero no cae en cuenta de toda la infraestructura y configuraciones que se hacen para poder tener acceso a algo muy usado hoy en día como una página web, mostrando los diferente tipos de red que se pueden crear, un ejemplo es entornos domésticos donde se pueden usar distintos elementos como cámaras de seguridad, televisores, consolas entre otros usando conexiones a internet para su interconexión.
De igual forma vemos una parte fundamental de la transmisión de datos ya que para los computadores la lengua nativa son 0 (falso) y 1(verdadero) llamado Bit el principal sistema que se usa para que se entiendan entre los diferentes dispositivos que hay en una red. Se hace un enfoque en los principales métodos de transmisión de datos, señales eléctricas que usa pulsos de electricidad, señales ópticas que usa pulsos de luz, señales inalámbricas que usan ondas de radio, donde se validan las diferencias de cada método, tocando un tema muy importante como lo es el ancho de banda (capacidad de un medio para transmitir datos de un punto a otro) y sus diferentes formas de medición como lo son Bps, Kbps, Mbps, Gbps, Tbps, dato con gran relevancia que se usa para el envío y recepción de toda la información que es necesaria para que funcione el internet
<img width="598" height="246" alt="Rendimiento ancho de banda" src="https://github.com/user-attachments/assets/44743ff4-4aee-4a54-91c9-241eb08e2ffb" />
# - Capitulo dos
## Componentes, tipos y conexiones de red
Se habla del término cliente servidor que hace parte fundamental de una red, ya que el cliente puede ser un equipo que está necesitando un servicio como correo electrónico, acceso a un archivo entre otros, el servidor es quien ofrece este servicio usando software dependiendo de la solicitud, se tiene varias alternativas para estos casos ya que un cliente puede servidor al mismo tiempo, pero se debe analizar cada cas para tener la claridad del uso que se le dará ala red para que el rendimiento del servicio sea el esperado, existen varias formas de interactuar entre cliente y servidor la mas sencilla es llamada entre pares o la mas recomendada un cliente que solicite servicios a varios servidores, para esto es necesario tener claro que la red esta divida en niveles de dispositivos en tres secciones como los son dispositivos finales(computadores, celulares, impresoras), dispositivos intermedios (switch,router, firewall) , medios de red (lan, wan, inalámbrico), el  siguiente paso es saber cómo realizar la conexión a internet de la red que se tenga para estos casos existen diferentes formas de realizarlo, por medio de un ISP quien será nuestro proveedor principal quien ya tiene las interconexiones necesarias entre otro ISP formando una gran red, con esto afinado se pasa a la parte de conexiones que se usaran para los usuarios finales, ya sea usando cable, red inalámbrica, red móvil o red satelital. 

<img width="588" height="277" alt="Componentes de red" src="https://github.com/user-attachments/assets/588a8927-0748-4614-9f12-70d5d1c2f5d4" />

# - Capitulo tres
Capa de aplicación
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


