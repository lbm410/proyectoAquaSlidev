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

**<v-click>Introducción a Aqua</v-click>**

- <v-click>Herramienta de JetBrains para pruebas automatizadas</v-click>
- <v-click>Facilita la gestión de pruebas en desarrollo de software</v-click>

<!-- Imagen: Diagrama general de pruebas de software -->

---

# Características Principales

**Características de Aqua**

- Interfaz intuitiva
- Soporte para múltiples tipos de pruebas
- Integración con CI/CD

<!-- Imagen: Captura de pantalla de la interfaz de Aqua -->
![Interfaz de Aqua](https://path-to-aqua-interface-screenshot.png)

---

# Instalación y Configuración

**Instalación y Configuración**

- Pasos para instalar Aqua
- Configuración inicial del proyecto

<!-- Imagen: Captura de pantalla del instalador de Aqua -->
![Instalador de Aqua](https://path-to-aqua-installer.png)

---

# Comparación con otras Herramientas

**Comparación con otras herramientas**

- Ventajas y desventajas
- Diferencias clave

<!-- Imagen: Tabla comparativa de Aqua con IntelliJ IDEA, Eclipse y Katalon Studio -->
![Tabla Comparativa](https://path-to-comparison-table.png)

---

# Configuración del Proyecto

**Configuración del Proyecto en Aqua**

- Estructura del proyecto
- Manejo de dependencias

<!-- Imagen: Captura de pantalla de un proyecto configurado en Aqua -->
![Configuración del Proyecto en Aqua](https://path-to-aqua-project-setup.png)

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
<!-- Imagen: Código de una prueba unitaria en Java -->

Ejecución de Pruebas
Ejecución de Pruebas

Visualización de resultados
Depuración de errores
<!-- Imagen: Captura de pantalla de la ejecución de pruebas en Aqua -->

Análisis de Cobertura
Análisis de Cobertura

Cobertura de código
Identificación de áreas no cubiertas
<!-- Imagen: Captura de pantalla del análisis de cobertura en Aqua -->

Caso Práctico
Caso Práctico

Aplicación de gestión de tareas
Configuración y ejecución de pruebas
<!-- Imagen: Diagrama o flujo de trabajo del caso práctico -->

Conclusiones
Conclusiones

Beneficios de usar Aqua
Mejora de la calidad del software
<!-- Imagen: Equipo de desarrollo trabajando -->

Preguntas y Respuestas
Preguntas y Respuestas

¿Dudas o comentarios?
<!-- Imagen: Icono de preguntas y respuestas -->