# Carreras

## Listado de entidades

### carreras **(ED)**

- carrera_id **(PK)**
- nombre
- tipo_carrera **(FK)**
- fecha
- tiempo
- mejor_tiempo
- altitud
- lugar
- pais **(FK)**
- foto

### tipos_carreras **(EC)**

- tipo_carrera **(PK)**
- descripcion
- distancia **(UQ)**

### paises **(EC)**

- pais_id **(PK)**
- nombre

## Relaciones

1. Una **carrera** _pertenece_ un **tipo de carrera**. (_1 a 1_)
2. Una **carrera** se _corre_ en un **país**. (_1 a 1_)


## Diagramas

### Modelo Entidad-Relación

![Modelo Entidad-Relación](ModeloE-R.png)

### Modelo Relacional de la base de datos

![Modelo Relacional de la base de datos](modeloRelacionalBD.png)

## Reglas de negocio

### carreras

1. Crear el registo de una carrera.
2. Leer el registro de una(s) carrera(s) dada una condición en particular.
3. Leer todos los registros de la entidad carreras.
4. Actualizar los datos de una carrera dada una condición en particular.
5. Eliminar los registros de una carrera dada una condición en particular.

### tipos_carreras

1. Todos los calores del atributo distancia, deberán estar expresados en _km_ y no se podrán repetir.
2. Crear el registo de un tipo de carrera.
3. Leer el registro de un(os) tipo(s) de carrera(s) dada una condición en particular.
4. Leer todos los registros de la entidad tipos carreras.
5. Actualizar los datos de un tipo de carrera dada una condición en particular.
6. Eliminar los registros de un tipo de carrera dada una condición en particular.

### paises

1. Crear el registo de un país.
2. Leer el registro de un(os) pais(es) dada una condición en particular.
3. Leer todos los registros de la entidad paises.
4. Actualizar los datos de un país dada una condición en particular.
5. Eliminar los registros de un país dada una condición en particular.
