---
title: Aqua de JetBrains
description: Herramienta Avanzada para Pruebas de Software
theme: academic
layout: figure-side
figureFootnoteNumber: 1
figureUrl: https://www.jetbrains.com/aqua/img/header-bg.svg
---
# Aqua de JetBrains

### Herramienta Avanzada para Pruebas de Software

**Herramientas y Métodos de la Ingeniería del Software**

<div style="position: absolute; bottom: 20%; width: 100%; text-align: left;">
  Lucas Barrientos Muñoz
</div>

<div style="position: absolute; bottom: 15%; width: 100%; text-align: left;">
  Diego Castañeda Cortés
</div>

<div style="position: absolute; bottom: 10%; width: 100%; text-align: left;">
  Abdelaziz Errabhi Rabtaoui
</div>

<Footnotes separator>
  <Footnote :number=1><a href="https://www.jetbrains.com/aqua/" rel="noreferrer" target="_blank">JetBrains</a></Footnote>
</Footnotes>


---
layout: figure
figureUrl: https://testsigma.com/blog/wp-content/uploads/Levels-of-testing-1.png
---

# Introducción

_**<v-click>Introducción a Aqua</v-click>**_

- <v-click>Herramienta de JetBrains para pruebas automatizadas</v-click>

  **<v-click>¿Qué es una prueba de software?</v-click>**


<!-- Imagen: Diagrama general de pruebas de software -->

---
layout: figure-side
figureUrl: https://www.jetbrains.com/aqua/img/Aqua_LP_videoPreview.png
figureX: 2099, 12212
figureCaption: Imagen oficial de JetBrains
figureFootnoteNumber: 2
---

# Características Principales

_**Características de Aqua**_

- <v-click>Interfaz intuitiva</v-click>
- <v-click>Integración con <v-mark class="red">CI/CD</v-mark></v-click>
- <v-click>Flujo de trabajo optimizado</v-click>
- <v-click>Enfoque especializado en testing</v-click>
- <v-click>Gestión de resultados y reportes</v-click>

<Footnotes separator>
  <Footnote :number=2><a href="https://www.jetbrains.com/aqua/" rel="noreferrer" target="_blank">JetBrains</a></Footnote>
</Footnotes>

---
layout: figure-side
figureUrl: https://i.postimg.cc/RZbpRHJc/Captura-de-pantalla-2024-05-28-103049.png
---

# Instalación y Configuración

**Instalación y Configuración**

<v-clicks depth="2">

- Descargamos Aqua
  - Configurar JDK
  - Configurar Plugins
- Creamos un proyecto Maven básico
  - Creamos una clase Calculator
  - Creamos el test CalculatorTest

</v-clicks>

---
layout: figure
figureUrl: https://i.postimg.cc/RZFS6bYC/image.png
figureCaption: Estructura del proyecto "proyectoAqua"
---

# Estructura del Proyecto




---


# Configuración del Proyecto

**Configuración del Proyecto en Aqua**

- <v-click>Estructura del proyecto</v-click>
- <v-click>Manejo de dependencias</v-click>
```xml {3-4|9-10|all}
<v-click>
  <dependencies>
      <dependency>
          <groupId>org.junit.jupiter</groupId>
          <artifactId>junit-jupiter-engine</artifactId>
          <version>5.8.2</version>
          <scope>test</scope>
      </dependency>
      <dependency>
          <groupId>org.junit.jupiter</groupId>
          <artifactId>junit-jupiter-api</artifactId>
          <version>5.8.2</version>
          <scope>test</scope>
      </dependency>
  </dependencies>
</v-click>
```


---

# Comparación con otras Herramientas

**Comparación con otras herramientas**

<v-clicks depth="2">

- IntelliJ Idea
  - Interfaz de usuario sofisticada y altamente personalizable
  - Similar integración con CI/CD a Aqua
  - Requiere una licencia
- Eclipse
  - Interfaz de usuario menos Junior-Friendly
  - Código abierto y amplia comunidad
  - Difícil integración con CI/CD
- Katalon Studio
  - Entorno robusto y fácil de usar
  - No requiere conocimientos profundos en programación
  - Opciones menos accesibles que en Aqua

</v-clicks>

---

# Creación de Pruebas Unitarias

**Pruebas Unitarias en Aqua**
```java
package org.proyectoAqua;

import ...

public class CalculatorTest {

    @Test
    public void testAddition() {
        Calculator calculator = new Calculator();
        int result = calculator.add(2, 3);
        assertEquals(5, result, "2 + 3 should equal 5");
    }

    @Test
    public void testSubtraction() {
        Calculator calculator = new Calculator();
        int result = calculator.subtract(5, 3);
        assertEquals(2, result, "5 - 3 should equal 2");
    }
}
```

---

# Creación de Pruebas Unitarias

**Clase Calculator para la realización de las pruebas**
```java
package org.proyectoAqua;

public class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    public int subtract(int a, int b) {
        return a - b;
    }
}

```
---
layout: figure
figureUrl: https://i.postimg.cc/FHzf9F5D/image.png
figureCaption: Resultado CalculatorTest en el IDE de Aqua
---

# Ejecución de las pruebas

**Captura del resultado de la ejecución**

---
layout: figure
figureUrl: https://i.postimg.cc/vmQGQ3VM/image.png
figureCaption: Resultado CalculatorTest en las pruebas de cobertura de Aqua
---

# Ejecución de las pruebas de cobertura

**Captura del resultado de la ejecución**

---
layout: figure
figureUrl: https://i.postimg.cc/2yTK775d/image.png
figureCaption: Informe de cobertura de los test proyecto
---

# Informe resultante de la cobertura

**Captura del resultado de la ejecución**

---
layout: figure
figureUrl: https://resources.jetbrains.com/help/img/idea/aqua_web_inspector_overview.png
figureCaption: Test de UI
figureFootnoteNumber: 3
---

# Testing para todos los niveles del desarrollo


<Footnotes separator>
  <Footnote :number=3><a href="https://www.jetbrains.com/aqua/" rel="noreferrer" target="_blank">Aqua Documentation</a></Footnote>
</Footnotes>

---
layout: figure
figureUrl: https://s3.eu-central-1.amazonaws.com/test-architect.dev/wp-content/uploads/2022/11/10152753/aqua_kinds_tests.png
figureCaption: Niveles de Testing
figureFootnoteNumber: 4
---

# Testing para todos los niveles del desarrollo


<Footnotes separator>
  <Footnote :number=4><a href="https://www.jetbrains.com/aqua/" rel="noreferrer" target="_blank">Aqua Documentation</a></Footnote>
</Footnotes>

---

# Muchas Gracias por su Atención

## ¿Alguna pregunta?



---