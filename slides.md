---
title: CryptCleaner
description: Proyecto de cifrado y descifrado en Python con AES
theme: academic
layout: figure-side
figureFootnoteNumber: 1
figureUrl: https://i.ibb.co/sPzZBXQ/DALL-E-2024-10-24-17-45-1.png
---

# CryptCleaner

### Implementación de Certificados Digitales

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
  - Crear un servidor legítimo con un certificado digital válido.  
  - Simular un servidor fraudulento con un certificado no autenticado.  
- *Relevancia*: Demostrar cómo los certificados digitales protegen contra ataques de suplantación.




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
figureUrl: https://i.ibb.co/yNYdnPr/Captura-de-pantalla-2024-11-28-181326.png
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

</v-clicks>

---
layout: figure-side
figureUrl: https://www.linuxadictos.com/wp-content/uploads/OpenSSL_logo.svg.png
---

# Conclusiones

**Implementación de Certificados Digitales**

<v-clicks depth="2">
  
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

