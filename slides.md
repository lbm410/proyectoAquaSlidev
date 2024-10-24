---
title: CryptCleaner
description: Proyecto de cifrado y descifrado en Python con AES
theme: academic
layout: figure-side
figureFootnoteNumber: 1
figureUrl: https://cdn-icons-png.flaticon.com/512/3470/3470475.png
---

# CryptCleaner

### Implementación de Cifrado y Descifrado con AES

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
figureUrl: https://i.ibb.co/njmSx3z/estructura.png
---

# Estructura del Proyecto

**Organización de archivos y carpetas**




---
layout: figure-side
figureUrl: https://i.ibb.co/RPd0hv5/main.png
figureFootnoteNumber: 2
---

# Función Principal

_**main.py**_

- <v-click>Solicita al usuario si desea cifrar o descifrar un archivo.</v-click>
- <v-click>Pide la ruta del archivo que el usuario desea procesar.</v-click>
- <v-click>Llama a las funciones `encrypt_file` o `decrypt_file` para realizar las operaciones correspondientes.</v-click>

<Footnotes separator>
  <Footnote :number=2><a href="https://docs.python.org/3/tutorial/inputoutput.html" rel="noreferrer" target="_blank">Input y Output en Python</a></Footnote>
</Footnotes>

---
layout: figure-side
figureUrl: https://i.ibb.co/0BtDQD2/encrypt.png
---

# Cifrado de Archivos

**Implementación de cifrado (encryptor.py)**

<v-clicks depth="2">

- Carga o genera una clave AES de 256 bits.
- Genera un Vector de Inicialización (IV).
- Cifra el contenido del archivo con AES en modo CFB.
- Guarda el archivo cifrado con la extensión `.enc`.

</v-clicks>


---
layout: figure-side
figureUrl: https://i.ibb.co/cb48xwq/decrypt.png
---

# Descifrado de Archivos

**Implementación de descifrado (encryptor.py)**

<v-clicks depth="2">
  
- Carga la clave AES que se utilizó durante el cifrado.
- Lee el IV desde los primeros 16 bytes del archivo cifrado.
- Descifra el contenido del archivo.
- Guarda el archivo desencriptado con el sufijo `_decrypted`.

</v-clicks>


---
layout: figure-side
figureUrl: https://i.ibb.co/B2RWZFG/key.png
figureFootnoteNumber: 3
---

# Gestión de Claves

_**Gestión segura de claves en AES**_

- <v-click>Si no existe una clave válida, se genera una nueva clave AES de 256 bits.</v-click>
- <v-click>La clave se guarda en el archivo `key.key` en formato hexadecimal.</v-click>
- <v-click>Para descifrar, la clave se carga y se convierte de hexadecimal a bytes.</v-click>

<Footnotes separator>
  <Footnote :number=3><a href="https://es.wikipedia.org/wiki/Advanced_Encryption_Standard" rel="noreferrer" target="_blank">AES</a></Footnote>
</Footnotes>


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
figureUrl: https://example.com/thanks.png
---

# Muchas Gracias

### ¿Alguna Pregunta?

---
