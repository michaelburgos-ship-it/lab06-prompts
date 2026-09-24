# Tarea: Mi prompt profesional
 
## Funcionalidad elegida
Diseño de un **Generador Automático de Rutinas de Ejercicio en Casa**. El sistema debe pedir datos básicos del usuario (como su nivel físico y tiempo disponible) y devolver una rutina organizada por días con ejercicios específicos, series y repeticiones sin necesidad de usar apps externas.
 
## Version 1: prompt basico
 
```text
Hazme una rutina de ejercicios para entrenar en casa.
```

### ¿Qué se evaluó y qué faltaba?
* **Qué cambié:** Se envió una petición extremadamente simple y directa.
* **Por qué:** Faltaba especificar para quién es la rutina, qué días entrenar, si hay equipo disponible y cómo estructurar la respuesta.
* **Qué mejoró:** La IA arrojó una lista gigante de ejercicios al azar, mezclando días y proponiendo ejercicios muy difíciles que requerían pesas de gimnasio, lo cual no era útil para la casa.

---
 
## Version 2
 
```text
Crea una rutina de ejercicios para hacer en casa de 3 días a la semana. Soy principiante y no tengo pesas. Dime qué hacer cada día.
```

### ¿Qué se evaluó y qué faltaba?
* **Qué cambié:** Añadí el nivel de dificultad (principiante), el lugar (casa) y la frecuencia (3 días).
* **Por qué:** Para evitar que la IA asuma que tengo equipo profesional o que puedo entrenar todos los días.
* **Qué mejoró:** La respuesta fue mucho más realista y adaptada a mi nivel. Sin embargo, los días venían desorganizados en párrafos largos de texto difíciles de leer a simple vista y no incluyó tiempos de descanso ni consejos de calentamiento.

---
 
## Version 3: prompt final
 
```text
Actúa como un Entrenador Personal Certificado y Experto en Calistenia (ejercicios con peso corporal).

Tu tarea es diseñar una rutina de entrenamiento estructurada para realizar en casa, ideal para un usuario de nivel principiante que no cuenta con mancuernas ni equipo de gimnasio.

Contexto: El usuario dispone de solo 30 minutos al día, 3 días a la semana (Lunes, Miércoles y Viernes). El objetivo principal es mejorar la condición física general de forma segura, previniendo lesiones.

Formato de salida requerido: Devuelve la información organizada en bloques independientes para cada día. Utiliza negritas para los nombres de los ejercicios y listas con viñetas claras. Incluye una sección final muy breve con 3 consejos obligatorios de calentamiento.

Restricciones obligatorias: 
- No sugieras ningún ejercicio que requiera barras, pesas o ligas de resistencia (usa solo el peso del cuerpo o muebles comunes como una silla).
- Cada sesión diaria no debe superar los 4 ejercicios en total.
```

### ¿Qué se evaluó y qué mejoró?
* **Qué cambié:** Incorporé los 5 componentes esenciales: Rol (entrenador), Instrucción (diseñar rutina), Contexto (30 min, principiante), Ejemplos y Formato, además de restricciones estrictas.
* **Por qué:** Para controlar con precisión la calidad y el orden de la rutina y evitar que la IA asuma datos por su cuenta.
* **Qué mejoró:** La respuesta de la IA fue perfecta. Entregó un plan visualmente impecable, fácil de seguir día por día, seguro para principiantes y adaptado al tiempo exacto disponible.

---
 
## Componentes del prompt final
 
| Componente | Fragmento del Prompt Final |
| --- | --- |
| **Rol** | "Actúa como un Entrenador Personal Certificado y Experto en Calistenia..." |
| **Instrucción** | "Tu tarea es diseñar una rutina de entrenamiento estructurada para realizar en casa..." |
| **Contexto** | "El usuario es principiante, no tiene equipo, dispone de 30 minutos al día, 3 días a la semana..." |
| **Ejemplos** | "Ejemplo de interacción esperada: Lunes (Torso): Flexiones inclinadas (3 series x 8 repeticiones)..." |
| **Formato** | "Devuelve la información organizada en bloques independientes para cada día... Usa negritas y viñetas." |

---
 
## Evaluacion del resultado
 
| Criterio de Evaluación | Cumplimiento (Sí / No) | Observación / Evidencia |
| --- | --- | --- |
| ¿La rutina está completamente libre de equipo o pesas? | **Sí** | Utilizó solo ejercicios con peso corporal y apoyo en sillas. |
| ¿Se dividió el entrenamiento exactamente en los 3 días solicitados? | **Sí** | Creó bloques separados para Lunes, Miércoles y Viernes. |
| ¿Cada día contiene un máximo de 4 ejercicios? | **Sí** | Cumplió la restricción de tiempo limitando la cantidad de movimientos. |
| ¿Se incluyó la sección de consejos de calentamiento al final? | **Sí** | Añadió las recomendaciones para evitar lesiones antes de empezar. |

---
 
## Errores que evite
 
* **Error 1: Ser demasiado general**
  * *Cómo lo evité:* En la versión 1 solo pedí "una rutina", lo que hizo que la IA me diera cosas imposibles. Lo solucioné detallando que el nivel es principiante, el tiempo máximo es de 30 minutos y los días exactos de la semana a entrenar.
* **Error 2: No indicar el formato de salida**
  * *Cómo lo evité:* En lugar de dejar que la IA redacte párrafos largos y aburridos, le ordené textualmente usar viñetas, bloques separados por días y nombres de ejercicios resaltados en **negrita** para que sea fácil de leer en el teléfono mientras se entrena.

- [Tarea: mi prompt profesional](lab06-prompts/TAREA.md)
