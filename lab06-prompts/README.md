# lab06-prompts
Bitacora de ingenieria de prompts

# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (escribe aqui cual usaste)
 
## Ejercicio 2: Tokens y ventana de contexto
 | Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 30  | 6 |
| desafortunadamente |19 | 5 |
Unas IA pueden guardar información de otros chats y usar estas en los nuevos, Gemini en este caso no puede, no cuenta con esto, no cuenta con esa memoria, por ello en el ejercicio si pudo responder mi pregunta en el chat donde le proporcione la información previamente y en el nuevo chat no pudo responderme
## Ejercicio 3: Temperatura
 
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------------------------------------|
| 0           | 100.0%         | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec   |
| 0.5         | 65.3%          | LibroYa, BiblioTec, LibroYa, PrestaLibro, LibroYa       |
| 0.5   | 65.3%          | BiblioTec, BiblioTec, LibroYa, BiblioTec, BiblioTec     |
| 1           | 44.5%          | LibroYa, LibroYa, BiblioTec, LibroYa, LibroYa           |
| 1.8         | 32.2%          | BiblioTec, NubeDeTinta, PrestaLibro, LibroYa, BiblioTec |

Al subir la temperatura, los porcentajes de elección se dispersan haciendo que los nombres generados sean mucho más variados y aleatorios en cada intento.El simulador nunca inventa un nombre nuevo porque las probabilidades se calculan estrictamente sobre la lista de nombres predefinida en el código.
## Ejercicio 4: Prompt vago vs estructurado
 | Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | Si| Si|
| Menciona a los usuarios principales |Si |Si |
| Tiene exactamente 3 funcionalidades | No|Si |
| Esta en 3 parrafos |No |Si |
| Lo usaria en un informe real |No |Si |

## Ejercicio 5: Anatomia de un prompt
| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java. Crea un programa en Java|
| Instruccion |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. |
| Ejemplo | |
| Formato | Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.Usando una clase Producto con los atributos codigo, nombre, precio y stock.Explica primero la estructura de la clase y luego presenta el codigo Java.Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).|


| Nivel | Componente Agregado | Impacto en la Respuesta de la IA |
| :---: | :--- | :--- |
| **1** | Ninguno (Prompt vago) | Genera un código genérico y básico (calculadora) sin especificaciones. |
| **2** | Rol (Desarrollador Java) | Adopta un estándar técnico aplicando POO y control de errores. |
| **3** | Instrucción específica | Restringe el código al dominio de la tienda usando una ID numérica. |
| **4** | Contexto detallado | Cambia a `String codigo`, forzando la búsqueda por texto y validación. |
| **5** | Ejemplo y Formato | Obliga a incluir explicación teórica previa y usar métodos específicos. |

 
## Ejercicio 6: Del prompt basico al profesional
| Qué revisar | Cumple (Sí / No) |
| --- | --- |
| ¿Está escrito en Java y usa Swing? | **Sí** |
| ¿Pide correo y contraseña? | **Sí** |
| ¿Explica el funcionamiento antes o después del código? | **Sí**|
| ¿El código está organizado en clases? | **Sí**  |
| ¿Valida los datos que ingresa el usuario? | **Sí** |
```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases. Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```
- [Bitacora de prompts](prompts/BITACORA.md)
