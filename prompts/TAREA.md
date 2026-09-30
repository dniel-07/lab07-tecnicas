# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para un formulario de registro de usuarios de una aplicación web.

## Version 1: prompt basico

Genera casos de prueba para un formulario de registro de usuarios.

## Version 2

```text
<rol>
Actúa como analista de pruebas de software especializado en aplicaciones web.
</rol>

<tarea>
Genera 8 casos de prueba para un formulario de registro de usuarios.
</tarea>

<contexto>
El formulario contiene los campos: nombre, correo electrónico y contraseña.
El correo debe tener un formato válido y la contraseña debe tener al menos
8 caracteres.
</contexto>

<formato>
Presenta los resultados en una tabla con las columnas:
ID, escenario, datos de entrada y resultado esperado.
</formato>
```

## Version 3: prompt final

```text
<rol>
Actúa como analista QA senior especializado en pruebas funcionales de
aplicaciones web. Explica los resultados de manera clara para un estudiante
de programación.
</rol>

<contexto>
Estoy probando un formulario web de registro de usuarios.

Campos:
- Nombre: obligatorio.
- Correo: obligatorio y debe tener un formato válido.
- Contraseña: obligatoria y debe tener al menos 8 caracteres.
- Confirmación de contraseña: debe coincidir con la contraseña.
</contexto>

<ejemplos>
Ejemplo de caso válido:
ID: TC01
Escenario: Registro con todos los datos correctos
Datos de entrada: Ana, ana@gmail.com, Clave1234, Clave1234
Resultado esperado: El usuario es registrado correctamente.

Ejemplo de caso inválido:
ID: TC02
Escenario: Correo con formato incorrecto
Datos de entrada: Ana, ana@, Clave1234, Clave1234
Resultado esperado: El sistema muestra un mensaje indicando que el correo no es válido.
</ejemplos>

<descomposicion>
Primero identifica los escenarios positivos y negativos que deben probarse.
Después genera 10 casos de prueba diferentes.
Finalmente revisa los casos para detectar duplicados o escenarios importantes
que hayan sido omitidos.
</descomposicion>

<formato>
Presenta los casos en una tabla con las columnas:
ID, tipo, escenario, datos de entrada y resultado esperado.
</formato>

<autocritica>
Después de crear la tabla, revisa tus propios casos de prueba.
Comprueba específicamente si incluiste:
1. Un registro completamente válido.
2. Campos obligatorios vacíos.
3. Un correo con formato inválido.
4. Una contraseña con menos de 8 caracteres.
5. Contraseñas que no coinciden.
6. Casos límite.
7. Casos duplicados.

Si falta alguno, agrega un nuevo caso e indica cuáles fueron agregados
durante la revisión.
</autocritica>
```

## Tecnicas usadas en el prompt final

|Técnica	|Parte del prompt	|Función|
|----|-----|-----|
|Role prompting	|rol	|Define que la IA responda como analista QA senior y adapte la explicación al estudiante.|
|Prompt estructurado|	rol, contexto, ejemplos, formato y autocritica|	Organiza las instrucciones para evitar que se mezclen.|
|Few-shot|	ejemplos|	Muestra ejemplos de casos válidos e inválidos para indicar el formato esperado.|
|Descomposición	|descomposicion|	Divide la tarea en identificación, generación y revisión.|
|Autocrítica	|autocritica|Hace que la IA revise los casos y busque omisiones o duplicados.|

## Evaluacion del resultado

|Criterio|	Cumple (Sí / No)|
|--------|--------------------|
|¿Utiliza el rol específico solicitado?|	Sí|
|¿Presenta los casos en la tabla solicitada?|	Sí|
|¿Incluye casos positivos y negativos?	|Sí|
|¿Incluye campos obligatorios vacíos?|	Sí|
|¿Incluye un correo con formato inválido?	|Sí|
|¿Incluye una contraseña menor a 8 caracteres?	|Sí|
|¿Incluye contraseñas que no coinciden?|	Sí|
|¿Realiza una autocrítica de los casos generados?	|Sí|
|¿Detecta posibles casos repetidos u omitidos?	|Sí|

## Por que elegi estas tecnicas

```text
Elegí role prompting, few-shot, descomposición, prompt estructurado y autocrítica porque la tarea consiste en generar casos de prueba que deben ser variados, ordenados y fáciles de revisar. El role prompting permite establecer el perfil de un analista QA, mientras que los ejemplos few-shot muestran exactamente el estilo esperado. La descomposición permite separar la identificación de escenarios de la generación de casos y la revisión. El prompt estructurado organiza las instrucciones y facilita que la IA respete el contexto y el formato. Finalmente, la autocrítica permite revisar la respuesta y buscar casos faltantes o repetidos. Estas técnicas son más útiles para esta tarea que utilizar únicamente un prompt corto, porque se necesita controlar tanto el contenido como la estructura y la revisión de los resultados.
```