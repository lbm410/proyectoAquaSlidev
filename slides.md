---
title: CryptCleaner
description: Proyecto de cifrado y descifrado en Python con AES
theme: academic
layout: figure-side
figureFootnoteNumber: 1
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# CryptCleaner

### Ransomware en un programa de limpieza de archivos basura

**Teoría de Códigos y Criptografía**

<div style="position: absolute; bottom: 20%; width: 100%; text-align: left;">
  Grupo 11
  <br>Lucas Barrientos Muñoz 
  <br>Ignacio López Miralles
</div>

<Footnotes separator>
  <Footnote :number=1><a href="https://es.wikipedia.org/wiki/Criptograf%C3%ADa" rel="noreferrer" target="_blank">Criptografía</a></Footnote>
</Footnotes>


---
layout: figure-side
figureUrl: https://i.ibb.co/zHB5JNm/Captura-de-pantalla-2024-11-28-175701.png
---

# Introducción

- *Objetivo*: Simular la distribución de ransomware utilizando criptografía aplicada.  
- *Enfoque*:  
  - Cifrar y Descifrar archivos de manera oculta en el equipo de la víctima. 
  - Enviar las claves por correo al atacante. 
  - Simular un servidor fraudulento con un certificado no autenticado.
  - Crear un instalador para el programa, ocultando el ransomware al antivirus de Windows.
- *Relevancia*: 
  - Demostrar cómo de importante es la criptografía en seguridad informática.




---
layout: figure-side
figureUrl: https://i.ibb.co/0M68P8d/2.png
figureFootnoteNumber: 2
---

# Función Decoy

_**gui.py**_

- <v-click>Muestra todas las opciones de un limpiador de archivos.</v-click>
- <v-click>Al pulsar en limpiar, ejecuta el ransomware.</v-click>
- <v-click>Llama a las funciones correspondientes para encriptar y solicitar el rescate.</v-click>

<Footnotes separator>
  <Footnote :number=2><a href="https://docs.python.org/3/library/tk.html" rel="noreferrer" target="_blank">TKinter en Python</a></Footnote>
</Footnotes>

---
layout: figure-side
figureUrl: https://i.ibb.co/F8CLCPZ/3.png
---

# Cifrado de Archivos

**Implementación de cifrado RSA (encryptor.py)**

<v-clicks depth="2">

- Genera una clave RSA de 256 bytes.
- Cifra la clave privada AES con la RSA generada.
- Guarda la clave pública en un archivo.
- Elimina posteriormente la clave pública del equipo objetivo.

</v-clicks>


---
layout: figure-side
figureUrl: https://i.ibb.co/cb48xwq/decrypt.png
---

# Descifrado de Archivos

**Implementación de descifrado (encryptor.py)**

<v-clicks depth="2">
  
- Carga la clave AES que se utilizó durante el cifrado y la desencripta con la RSA.
- Lee el IV desde los primeros 16 bytes del archivo cifrado.
- Descifra el contenido del archivo.
- Guarda el archivo desencriptado con el sufijo `.decrypted`.

</v-clicks>

---
layout: figure-side
figureUrl: https://i.ibb.co/RHv3kBx/1.png
---

# Envío de Correos Electrónicos

**Implementación de envío de correos (email_utils.py)**

<v-clicks depth="2">
  
- Utiliza la librería smtplib para el envío de mails por smtp.
- Utiliza la librería EmailMessage para el contenido del mail.
- Envía el archivo de la clave pública RSA.

</v-clicks>


---
layout: figure-side
figureUrl: https://i.ibb.co/7R6Jhc1/Captura-de-pantalla-2024-11-28-180541.png
figureFootnoteNumber: 2
---

# Funcionalidades con Certificados

_**Servidor Legítimo**_

- <v-click>Utiliza HTTPS y un certificado firmado por una CA interna.</v-click>

_**Servidor Falso**_

- <v-click>Simula un sitio de phishing con un certificado autofirmado.</v-click>

_**Cliente Verificador**_

- <v-click>Llama a las funciones correspondientes para encriptar y solicitar el rescate.</v-click>

<Footnotes separator>
  <Footnote :number=2><a href="https://www.pyopenssl.org/en/latest/l" rel="noreferrer" target="_blank">pyOpenSSL en Python</a></Footnote>
</Footnotes>

---
layout: figure-side
figureUrl: https://i.ibb.co/NTtL8fd/Captura-de-pantalla-2024-11-28-180756.png
---

# Desarrollo Técnico

<v-clicks depth="2">

### Configuración de servidores
- *Servidor legítimo*:  
  - Configurado con Flask.  
  - Usa un certificado firmado por la CA del proyecto.
- *Servidor falso*:  
  - Estructura similar, pero utiliza un certificado autofirmado.

### Certificados digitales
- *Certificado de la CA*: Firma el certificado del servidor legítimo.  
- *Certificados de los servidores*: Incluyen clave pública, nombre del propietario y firma.

</v-clicks>


---
layout: figure-side
figureUrl: https://i.ibb.co/Ltq6sgw/Captura-de-pantalla-2024-12-19-113701.png
---

# Resultados

<v-clicks depth="2">
  
### Verificación de certificados
- *Servidor legítimo*: El cliente permitió la descarga tras verificar la autenticidad del certificado.  
- *Servidor falso*: El cliente alertó al usuario sobre el riesgo de la conexión.

### Comportamiento del cliente
- Respuesta adecuada en ambos casos:  
  - Descarga segura desde el servidor legítimo.  
  - Advertencias antes de interactuar con el servidor falso.
  - Instalación segura del cliente de limpieza maligno.

</v-clicks>

---
layout: figure-side
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# Conclusiones

**Ransomware CryptCleaner**

<v-clicks depth="2">
  
- Se ha implementado un sistema de cifrado y descifrado oculto al usuario.
- Los certificados digitales son críticos para garantizar la seguridad en las comunicaciones.
- Este proyecto ilustra la importancia de la criptografía aplicada en escenarios prácticos.
- **Lección clave**: La educación del usuario es esencial para reducir riesgos en conexiones inseguras.

</v-clicks>


---
layout: figure
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# Muchas Gracias

### ¿Alguna Pregunta?

