 Chat punto a punto por Wi-Fi con transferencia de archivos

 Descripción

Este proyecto implementa una aplicación en Python que permite la comunicación entre dos computadoras mediante una conexión Wi-Fi usando sockets TCP.
Incluye un chat cliente-servidor y una mejora opcional para transferencia de archivos.

---

Objetivo

Desarrollar un sistema de comunicación punto a punto que funcione en red local (misma red o hotspot), permitiendo:

* Envío y recepción de mensajes en tiempo real
* Transferencia de archivos (opcional)
* Registro de eventos y pruebas

---

 Requisitos

* Python 3.8 o superior
* Dos computadoras conectadas a la misma red Wi-Fi o hotspot
* Sistema operativo: Windows / Linux

Instalar dependencias:

```bash
pip install -r requirements.txt
```

---

## 📂 Estructura del proyecto

```
chat-wifi/
│
├── src/
│   ├── server_chat.py
│   ├── client_chat.py
│   ├── file_transfer.py
│   └── utils.py
│
├── docs/
├── images/
├── results/
└── scripts/
```

---

 Configuración de red

1. Conectar ambas computadoras a:

   * La misma red Wi-Fi, o
   * Un hotspot creado desde una de ellas

2. Obtener la IP del servidor:

Windows:

```bash
ipconfig
```

Linux:

```bash
ifconfig
```

---

 Ejecución

### 1. Iniciar servidor

```bash
python src/server_chat.py
```

---

### 2. Iniciar cliente

Editar en `client_chat.py` la IP del servidor:

```python
HOST = "192.168.X.X"
```

Ejecutar:

```bash
python src/client_chat.py
```

---

Uso del chat

* El cliente envía mensajes al servidor
* El servidor responde desde la terminal
* Comunicación en tiempo real mediante TCP

---

Transferencia de archivos (opcional)

Permite enviar archivos del cliente al servidor mediante un protocolo simple:

Formato de encabezado:

```
FILENAME | SIZE | SHA256
```

Flujo:

1. Cliente envía metadatos
2. Servidor responde READY
3. Cliente envía archivo
4. Servidor valida y responde OK o ERR

Archivos recibidos:

```
results/received/
```

---

## 🧪 Pruebas realizadas

* Conexión en misma red Wi-Fi
* Conexión mediante hotspot
* Envío de mensajes exitoso
* Transferencia de archivos (si aplica)

Evidencias en:

```
images/tests/
```

Logs en:

```
results/logs/
```

---

 Seguridad

* Comunicación en texto plano (sin cifrado)
* Se recomienda no usar redes públicas
* Cerrar puertos después de las pruebas

---

 Documentación

* THEORY.md → fundamentos de redes y sockets
* DECISION.md → decisiones de implementación
* LEARNED_PYTHON.md → conceptos aprendidos

---

 Autores

herrera hernandez jose angel
sanchez flores javier martin
hernandez dimas leonel 
llanos andrade emmanuel
delgado islas zuriel ignacio
torres duarte michell
---

