# Sigue los pasos — Cuaderno de demostración
Carga de datos de forma incremental con COPY INTO
El cuaderno de demostración te guía a través de la creación de una tabla vacía con un esquema definido, la carga de datos mediante COPY INTO y la ejecución repetida del mismo comando para demostrar su idempotencia. El proceso omite los archivos que ya han sido cargados.

## Lo que harás:
- Crear una tabla vacía con definiciones de columnas explícitas.
- Ejecutar COPY INTO para cargar todos los archivos CSV desde el volumen (6 filas).
- Volver a ejecutar el mismo comando COPY INTO y observar que no se ven afectadas filas adicionales (0 filas afectadas).
- Consultar DESCRIBE HISTORY para confirmar que solo se realizó una operación de carga.
- Pruébalo — Cuaderno de ejercicios
- Carga datos en tu propia tabla utilizando COPY INTO
- Crea una tabla llamada `practice_copyinto` y utiliza COPY INTO para cargar los archivos CSV. Verifica el número de filas y vuelve a ejecutar el comando para confirmar su idempotencia.

## Lo que practicarás:
- Crear una tabla vacía con un esquema definido.
- Redactar una sentencia COPY INTO incluyendo opciones de formato.
- Verificar el comportamiento idempotente mediante la reejecución del comando.
- Consultar el historial de versiones.

# Conclusión
Lo que has aprendido
- COPY INTO carga archivos nuevos y omite aquellos que ya han sido procesados ​​(comportamiento idempotente).
- Es necesario crear primero una tabla vacía y luego cargar los datos en ella; a diferencia de CTAS, que realiza ambas acciones simultáneamente.
- Es seguro ejecutarlo de forma programada: si no llegan archivos nuevos, no ocurre ningún cambio.
- El historial de versiones permite confirmar qué operaciones de carga modificaron realmente los datos.