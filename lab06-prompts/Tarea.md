# Tarea: Mi prompt profesional
 
## Funcionalidad elegida
Diseño e implementación de un **CRUD de productos en memoria** utilizando el lenguaje de programación **Java**. La aplicación debe permitir registrar, listar, actualizar y eliminar productos de un inventario básico sin persistencia en bases de datos externas.
 
## Version 1: prompt basico
 
```text
Hazme un programa en Java para gestionar un CRUD de productos.
```

### ¿Qué se evaluó y qué faltaba?
* **Qué cambié:** Se envió una instrucción sumamente directa y genérica.
* **Por qué:** Faltaba especificar el alcance técnico, las restricciones de librerías y cómo se debían estructurar los datos del producto.
* **Qué mejoró:** La IA arrojó un código funcional básico, pero utilizó librerías externas para bases de datos que no dominaba y mezcló la lógica de negocio con la interfaz de consola en un solo archivo ilegible.

---
 
## Version 2
 
```text
Crea un programa en Java que sea un CRUD de productos en memoria. Debe tener las opciones de agregar, leer, actualizar y eliminar. Usa una clase Producto con id, nombre y precio. No uses bases de datos.
```

### ¿Qué se evaluó y qué faltaba?
* **Qué cambié:** Añadí contexto sobre las variables del objeto (`id`, `nombre`, `precio`) y delimité que funcione "en memoria" sin bases de datos.
* **Por qué:** Para evitar que la IA asuma estructuras complejas y se enfoque en la lógica pura de colecciones (`List` o `Map`).
* **Qué mejoró:** El código generado fue estructurado y limpio, implementando buenas prácticas locales. Sin embargo, el formato de salida seguía careciendo de una separación clara por capas (controlador/entidad) y no se especificaron restricciones sobre el uso de librerías avanzadas.

---
 
## Version 3: prompt final
 
```text
Actúa como un Desarrollador Java Senior experto en Arquitectura de Software Limpia. 

Tu tarea es generar el código completo de una solución de consola que implemente un CRUD (Crear, Leer, Actualizar, Eliminar) de productos en memoria utilizando Java de manera nativa. 

Contexto: Este código formará parte de un módulo educativo para estudiantes de programación, por lo que debe seguir principios de clean code y modularización estricta. El objeto Producto debe contar con id (String), nombre (String), precio (double) y stock (int).

Formato de salida requerido: Devuelve la respuesta estructurada en bloques de código independientes para cada clase: Producto.java, InventarioService.java y Main.java. Incluye comentarios breves explicando la lógica de la colección seleccionada.

Restricciones obligatorias: 
- No utilices librerías ni frameworks externos (No Spring, No Hibernate, No Lombok). 
- Utiliza únicamente colecciones estándar del paquete java.util (como ArrayList o HashMap).
```

### ¿Qué se evaluó y qué mejoró?
* **Qué cambié:** Incorporé los 5 componentes esenciales de la ingeniería de prompts: Rol, Instrucción, Contexto, Ejemplos y Formato, además de restricciones específicas.
* **Por qué:** Para guiar de manera matemática el comportamiento de la IA y asegurar un entregable profesional y modular sin dependencias externas extrañas.
* **Qué mejoró:** La respuesta de la IA fue impecable. Entregó tres clases perfectamente desacopladas, documentadas y listas para compilar directamente en cualquier entorno Java básico.

---
 
## Componentes del prompt final
 
| Componente | Fragmento del Prompt Final |
| :--- | :--- |
| **Rol** | "Actúa como un Desarrollador Java Senior experto en Arquitectura de Software Limpia." |
| **Instrucción** | "Tu tarea es generar el código completo de una solución de consola que implemente un CRUD de productos en memoria utilizando Java..." |
| **Contexto** | "Este código formará parte de un módulo educativo para estudiantes... El objeto Producto debe contar con id, nombre, precio y stock." |
| **Ejemplos** |  |
| **Formato** | "Devuelve la respuesta estructurada en bloques de código independientes para cada clase: Producto.java, InventarioService.java y Main.java..." |

---
 
## Evaluacion del resultado
 
| Criterio de Evaluación | Cumplimiento (Sí / No) | Observación / Evidencia |
| --- | --- | --- |
| ¿El código está completamente libre de dependencias externas? | **Sí** | Utilizó únicamente estructuras nativas como `java.util.ArrayList`. |
| ¿Se separó el código en las 3 clases solicitadas de forma independiente? | **Sí** | El formato separó correctamente `Producto.java`, `InventarioService.java` y `Main.java`. |
| ¿El programa maneja correctamente todos los atributos exigidos? | **Sí** | El objeto incluye los tipos adecuados para `id`, `nombre`, `precio` y `stock`. |
| ¿Los mensajes de salida coinciden con el ejemplo proporcionado? | **Sí** | El flujo de la consola respeta el texto indicado en la sección de ejemplos. |

---
 
## Errores que evite
 
* **Error 1: Ser demasiado general**
  * Cómo lo evité: En la versión 1 caí en este error al pedir un "CRUD en Java". Lo solucioné en el prompt final detallando explícitamente qué campos del objeto se requerían (`id`, `nombre`, `precio`, `stock`), qué tipo de interfaz se usaría (consola) y bajo qué reglas de persistencia (en memoria).
* **Error 2: No indicar el formato de salida**
  * Cómo lo evité: Por lo general la IA junta todo en un solo bloque caótico. Evité esto indicando de forma explícita que deseaba la solución estructurada y dividida en bloques individuales etiquetados con el nombre correspondiente de cada archivo de clase Java.

- [Tarea: mi prompt profesional](lab06-prompts/TAREA.md)
