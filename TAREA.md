# Tarea: Mi prompt avanzado

## diseñar las clases de un sistema de notas

## Version 1: prompt basico

```text
(creame un clases para un sistema de notas)
```

Aplique la tecnica de zero-shot porque necesitaba ver como responde la ia a mi prompt.

## Version 2: prompt medio

```text
(creame un clases para un sistema de notas.Siguendo los siguientes ejemplos.
Pepito tiene  13 en su nota final esta aprobado
Juanita tiene 10 en su nota final esta desaprobada
Paco tiene 11 en su nota final tiene que ir a recuperacion)
```

Aplique la tecnica few-shot porque gracias a los ejemplos la ia puede entender como quiero que me de el codigo
lo que mejoro en el codigo que el anterior es solo se usaron dos clases uno para el estudiante y otro para las notas

## Version 3: prompt final

```text
(<rol>Actúa como un Profesor Titular de Programación Orientada a Objetos en Java.<rol>
<tarea>Diseña  un sistema de control de notas en Java dividiendo el desarrollo en los siguientes pasos:
1. Define una clase `Estudiante` que sea nombre, nota y sus métodos getter/setter.
2. Define una clase `SistemaNotas` que gestione una lista de estudiantes usando Scanner y un bucle `while` para registrar múltiples alumnos.
3. Clasifica la condición según las siguientes reglas:
   - Nota de 13 a 20: "Aprobado" (Ejemplo: Juanito con 14 esta aprobado)
   - Nota de 11 a 12: "Recuperación" (Ejemplo: Pedro con 11 esta recuperación)
   - Nota de 0 a 10: "Desaprobado" (Ejemplo: Maria con 09 esta desaprobado)
4. Incluye un método `main` ejecutable para probar el sistema.<tarea>

<formato>Proporciona el código organizado claramente en bloques por cada clase, incluyendo comentarios explicativos en los métodos principales.<formato>

<autocritica>revisa si el código incluye instancias estáticas innecesarias de datos de estudiantes. Si existen, elimínalas y asegúrate de que todo el registro se usando Scanner.<autocritica>)
```

Aplique Role Prompting, Prompt Estructurado, Descomposición, Few-Shot y Autocrítica porque con este prompt puedo pedir a la ia que me el codigo tal como lo quiero y con la autocritica puedo correjir si veo un error. Lo que mejoro en comparacion a los codigos anteriores es que se usan dos clases donde puedo poner la nota de los alumnos y agregar a varios alumnos sin tener que reiniciar el programa

## Tecnicas usadas en el prompt final

| Tecnica usada       | Parte del prompt final correspondiente                                                                                                                               |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Role Prompting      | Actúa como un Profesor Titular de Programación Orientada a Objetos en Java.                                                                                          |
| Descomposición      | diseña un sistema... dividiendo el desarrollo en los siguientes pasos                                                                                                |
| Few-Shot Prompting  | (Ejemplo: Juanito con 14 esta aprobado) (Ejemplo: Pedro con 11 esta recuperación)                                                                                    |
| Prompt Estructurado | Uso de etiquetas como rol, tarea y formato de salida                                                                                                                 |
| Autocrítica         | revisa si el código incluye instancias estáticas innecesarias de datos de estudiantes. Si existen, elimínalas y asegúrate de que todo el registro se usando Scanner. |

## Evaluacion del resultado

| Criterios                                                                   | Correcta (Si/No) |
| --------------------------------------------------------------------------- | ---------------- |
| ¿El código generado compila y ejecuta correctamente en Java?                | Si               |
| ¿El sistema permite registrar múltiples alumnos mediante un bucle?          | Si               |
| ¿El codigo cumple exactamente con las reglas indicadas?                     | Si               |
| ¿El código está separado adecuadamente en clases aplicando encapsulamiento? | Si               |

## Por que elegi estas tecnicas

Elegí las tecnicas de Role Prompting, Prompt Estructurado, Descomposición, Few-Shot y Autocrítica porque abordan de manera integral los problemas habituales al generar código con IA. El Role Prompting establece un estándar de calidad académico. La Descomposición y el Prompt Estructurado guían al modelo para evitar omitir partes clave del programa. Few-Shot ayuda a que la ia tenga ejemplos en que basarse, mientras que la Autocrítica previene que el codigo devuelva ejemplos con datos erroneos y haciendo que agrege nuevas peticiones.
