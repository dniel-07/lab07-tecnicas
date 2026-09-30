# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 | "1. Positivo" | Sí |
| One-shot | 5 | "1. Positivo" | Sí |
| Few-shot | 5 | "Me encanto, llego rapido" | Sí |

## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo | 318.60 | No | Sí|
| Paso a paso | 318.60 | Sí | Sí |

Ver el razonamiento permite comprobar cada cálculo y detectar posibles errores, incluso cuando la respuesta final es correcta. También ayuda a entender el método para poder aplicarlo correctamente a problemas similares.

## Ejercicio 4: Role prompting

| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | sencillo | ejemplos | estudiantes |
| B. Rol docente | sencillo | codigo | profesores |
| C. Rol senior | tecnico | codigo | desarrolladores |

## Ejercicio 5: Descomposicion

|Paso	|Mensaje|
|--------|------|
|1|	Voy a crear un sistema de inventario para una tienda pequena en Java. Lista los 5 requisitos principales del sistema.|
|2	|Con esos requisitos, disena las clases necesarias. Para cada clase indica sus atributos con su tipo de dato.|
|3	|Escribe el codigo Java de la clase Producto con sus atributos, un constructor y los metodos get y set.|
|4|	Revisa el codigo de la clase Producto y propone 3 mejoras concretas.|

## Ejercicio 6: Prompt estructurado y autocritica

```text
PROMPT ESTRUCTURADO
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>

AUTOCRITICA
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```

|Qué revisar	|Cumple (Sí / No)|
|-----|------|
|¿Tiene las 4 columnas pedidas?|	Sí|
|¿Incluye el bloqueo después de 3 intentos?	|Sí|
|¿Incluye casos con campos vacíos?	|Sí|
|¿Indica qué casos agregó en la autocrítica?	|Sí|
|¿Hay algún caso repetido o que no tenga sentido?	|No|


