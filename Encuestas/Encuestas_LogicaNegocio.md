# Encuestas

## Listado de entidades

### encuestas **(ED)**

- encuesta_id **(PK)**
- nombre
- descripcion
- imagen
- fecha
- encuestados

### preguntas **(ED)**

- pregunta_id **(PK)**
- encuesta_id **(FK)**
- pregunta

### Respuestas **(ED)**

- respuesta_id **(PK)**
- pregunta_id **(FK)**
- respuesta
- es_correcto

### encuestados **(ED)**

- encuestado_id **(PK)**
- nombre
- apellidos
- edad
- email **(UQ)**

### resultados **(ED/EP)**

- resultado_id **(PK)**
- encuesta_id **(FK)**
- encuestado_id **(FK)**
- preguntas
- correctas

## Relaciones

1. Una **encuesta** tiene **preguntas** (_1 a M_)
2. Una **pregunta** tiene **respuestas** (_1 a M_)
3. Una **encuesta** tiene **resultados** (_1 a M_)
4. Un **encuestado** tiene **resultado** (_1 a M_)

## Reglas de Negocio

### Encuestas

1. Crear una encueesta.
2. Leer todas las encuestas.
3. Actualizar una encuesta.
4. Eliminar una encuesta.
5. Aumentar en 1 el valor del atributo **encuestados** cada que un encuestado complete la encuesta.

### Preguntas

1. Crear una pregunta.
2. Leer todas las preguntas.
3. Leer una pregunta en particular.
4. Actualizar una pregunta.
5. Eliminar una pregunta.

### Respuestas

1. Crear una respuesta.
2. Leer todas las respuestas.
3. Leer una respuesta en particular.
4. Actualizar una respuesta.
5. Eliminar una respuesta.

### Encuestados

1. Crear un encuestado.
2. Leer todos los encuestados.
3. Leer un encuestado en particular.
4. Actualizar un encuestado.
5. Eliminar un encuestado.
6. Antes de crear un encuestado, verificar que no exista un encuestado con el mismo email.


### Resultados

1. Crear un resultado.
2. Leer todos los resultados.
3. Leer un resultado en particular.
4. Actualizar un resultado.
5. Eliminar un resultado.
6. Sacar el porcentaje de acertividad que tuvo un encuestado al contestar una encuesta.
