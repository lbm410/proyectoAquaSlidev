---
title: CryptCleaner
description: Proyecto de cifrado y descifrado en Python con AES
theme: academic
layout: figure-side
figureFootnoteNumber: 1
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# CryptCleaner

### Implementación de Cifrado y Descifrado RSA y UI

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
layout: figure
figureUrl: https://i.ibb.co/6ZcJMgL/1.png
---

# Estructura del Proyecto

**Organización de archivos y carpetas**




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
layout: slide
---

# Logs y Manejo de Errores

**Seguimiento del programa con logs**

- <v-click>Registro de eventos importantes como la carga o generación de claves.</v-click>
- <v-click>Mensajes detallados para depuración cuando ocurren errores.</v-click>
- <v-click>Manejo de excepciones para garantizar que el programa no falle sin notificar al usuario.</v-click>

---
layout: figure
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# Muchas Gracias

### ¿Alguna Pregunta?

---
