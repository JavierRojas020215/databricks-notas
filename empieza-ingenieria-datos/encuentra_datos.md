# Introducción
Navegue por la jerarquía del catálogo, localice un archivo de datos sin procesar, previsualice su contenido y cree una tabla Delta a partir de él.
Observe cómo navegar por la jerarquía de Unity Catalog, encontrar un archivo CSV en un volumen, previsualizar su contenido mediante `read_files` y crear una tabla Delta utilizando `CREATE TABLE AS SELECT`.

## Siga las instrucciones: Notebook de demostración
Recorra el notebook de la lección paso a paso.
El notebook de demostración le guiará a través de cada paso mostrado en el vídeo. Confirmará el contexto de su catálogo y esquema, listará los archivos en su volumen, previsualizará los datos CSV sin procesar y creará la tabla `employees`; todo ello ejecutando las celdas en orden.
Lo que hará:
- Ejecutar `SELECT current_catalog(), current_schema();` para confirmar su entorno.
-Utilizar `LIST` para ver los archivos CSV en el volumen `myfiles`.
-Previsualizar los datos sin procesar mediante `read_files`.
-Crear la tabla Delta `employees` utilizando `CREATE TABLE AS SELECT`.
-Verificar la tabla mediante SQL y el Explorador de catálogos (Catalog Explorer).

## Pruébelo: notebook de práctica
Cree una tabla por su cuenta a partir de un archivo CSV diferente.
Ahora, inténtelo sin la guía paso a paso. El notebook de práctica le proporciona un segundo archivo CSV (`employees2.csv`) y le pide que cree una nueva tabla llamada `new_employees`. Cada tarea incluye una pista desplegable por si se queda bloqueado.
Lo que practicará:
- Previsualizar un archivo CSV diferente.
- Redactar su propia sentencia `CREATE TABLE AS SELECT`.
- Verificar que la tabla existe.

# Conclusión
Lo que ha aprendido
Navegar por la jerarquía de Unity Catalog (catálogo → esquema → volumen).
Previsualizar datos CSV sin procesar mediante `read_files`.
Crear una tabla Delta utilizando `CREATE TABLE AS SELECT`.
Verificar tablas tanto mediante SQL como en el Explorador de catálogos (Catalog Explorer).