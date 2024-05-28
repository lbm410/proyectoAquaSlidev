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
figureFootnoteNumber: 3
figureCaption: Creación del proyecto **"proyectoAqua"**
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
layout: figure-side
figureUrl:  https://www.jetbrains.com/aqua/img/Aqua_LP_videoPreview.png
---


# Configuración del Proyecto

**Configuración del Proyecto en Aqua**

- Estructura del proyecto
- Manejo de dependencias
```xml {3-4|9-10|all}
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
```


---

# Comparación con otras Herramientas

**Comparación con otras herramientas**



<!-- Imagen: Tabla comparativa de Aqua con IntelliJ IDEA, Eclipse y Katalon Studio -->
![Tabla Comparativa](https://path-to-comparison-table.png)

---

# Creación de Pruebas Unitarias

**Pruebas Unitarias en Aqua**

- Ejemplo con JUnit
- Configuración de pruebas

```java
package org.proyectoAqua;

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

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
´´´