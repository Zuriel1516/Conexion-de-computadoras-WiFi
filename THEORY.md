**THEORY**
**Autor-Emmanuel**
¿Qué es un socket?
Un socket es un punto de comunicación entre dos dispositivos en red. Permite enviar y recibir datos usando una dirección IP y un puerto.
Ejemplo:
Un cliente (la app) se conecta al servidor web mediante un socket para pedir una página.

TCP vs UDP
TCP (Transmission Control Protocol)
Conexión establecida (hay “handshake”)
Garantiza entrega y orden de los datos
Más lento pero confiable

Cuándo usarlo:

Navegación web (HTTP/HTTPS)
Correos electrónicos
Transferencia de archivos
UDP (User Datagram Protocol)
No hay conexión previa
No garantiza entrega ni orden
Más rápido y ligero

Cuándo usarlo:

Videojuegos online
Streaming
Videollamadas
Puertos y direcciones IP
IP: Identifica el dispositivo en la red (como una dirección de casa)
Puerto: Identifica el servicio dentro del dispositivo (como el número de habitación)
Puertos bien conocidos (0–1023):
80 → HTTP
443 → HTTPS
21 → FTP
25 → SMTP
Puertos registrados (1024–49151):
Usados por aplicaciones específicas
Puertos dinámicos (49152–65535):
Se asignan temporalmente para conexiones
NAT y problemas de conectividad

NAT (Network Address Translation):
Permite que varios dispositivos usen una sola IP pública.

Problemas:

Dificulta conexiones directas (ej. juegos P2P)
Necesitas abrir puertos (port forwarding)
Puede causar fallas en apps que requieren conexión entrante
Firewalls y permisos de puerto

Un firewall controla qué conexiones entran o salen.

Bloquea tráfico no autorizado
Permite abrir puertos específicos

Ejemplo:
Si tienes un servidor en tu PC, debes abrir el puerto (ej. 8080) para que otros puedan conectarse.

Wi-Fi Direct vs Hotspot vs Misma red
Wi-Fi Direct
Conexión directa entre dispositivos
No necesita router
Limitado en compatibilidad
Hotspot (punto de acceso)
Un dispositivo comparte internet
Actúa como router
Puede generar NAT
Misma red (LAN)
Todos conectados al mismo router
Comunicación más sencilla y directa
Ideal para pruebas locales
Seguridad básica (TLS/SSL)
TLS/SSL: Protocolos que cifran la comunicación
Protegen datos (contraseñas, información personal)

Recomendaciones para pruebas:

Usar HTTPS siempre que se pueda
No abras puertos innecesarios
Prueba en red local antes de internet
Usa contraseñas seguras
Evita exponer servicios sin autenticación
