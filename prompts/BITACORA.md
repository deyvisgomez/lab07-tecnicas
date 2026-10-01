# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.

Herramienta de IA usada: (Gemini)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta                                              | Todas con el mismo formato (Si/No) |
| --------- | --------------- | -------------------------------------------------------------------- | ---------------------------------- |
| Zero-shot | 5               | clasificacion en negrita y una breve explicacion                     | si                                 |
| One-shot  | 5               | comentario en negrita a lado de una flecha con la clasificacion      | si                                 |
| Few-shot  | 5               | comentarios entre comillad a lado de una flecha con la clasificacion | si                                 |

## Ejercicio 3: Chain of Thought

| Pedido      | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
| ----------- | ------------------ | ------------------------- | ---------------- |
| Directo     | 106.2              | No                        | No               |
| Paso a paso | 318.60             | Si                        | Si               |

## Ejercicio 4: Role prompting

| Version        | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas            |
| -------------- | ------------------------------ | --------------------- | ------------------------------- |
| A. Sin rol     | sencillo                       | si                    | A un programador principiante   |
| B. Rol docente | sencillo                       | si                    | A un estudiante de programacion |
| C. Rol senior  | tecnico                        | si                    | A un programador graduado       |

## Ejercicio 5: Descomposicion

Paso 1: La ia me entrego como resultado los 5 requisitos que le pedi para el programa en java.

Paso 2: Separo los requisitos en 5 clases por requisito ademas de agregar sus atributos.

Paso 3: Me dio todo el codigo de la clase producto ya escrito con sus get,letter y get.

Paso 4: La ia agrego 3 mejoras en la clase producto siendo agregar validacion de negocio, sobrescribir y encapsular opereciones de actualizacion de stocks

Comparacion: a diferencia de la respuesta que me dio al pedir todo en un solo paso, la ia no solo no me dio el codigo en java si no que fue complicado de entender la respuesta

## Ejercicio 6: Prompt estructurado y autocritica

| Qué revisar                                      | Correcta (Si/No) |
| ------------------------------------------------ | ---------------- |
| ¿Tiene las 4 columnas pedidas?                   | Si               |
| ¿Incluye el bloqueo después de 3 intentos?       | Si               |
| ¿Incluye casos con campos vacíos?                | Si               |
| ¿Indica qué casos agregó en la autocrítica?      | Si               |
| ¿Hay algún caso repetido o que no tenga sentido? | Si               |

```text
(<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>
Autocrítica:
 Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contraseña con espacios? Agrega los que falten e indica cuales agregaste.
)
```
