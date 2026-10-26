# Sigue los pasos — Notebook de demostración
Construye el pipeline completo: Bronze → Silver → Gold
El notebook de demostración te guía a través de toda la arquitectura Medallion en una sola sesión. Crearás una tabla Bronze con datos sin procesar (raw data), la transformarás en una tabla Silver con valores estandarizados y marcas de tiempo (timestamps), construirás una tabla de agregación Gold y, finalmente, explorarás cómo Unity Catalog rastrea automáticamente el linaje (lineage) a través de las tres capas.

## Lo que harás:
- Listar los archivos CSV en el volumen.
- Crear la tabla `current_employees_bronze` y cargar datos mediante `COPY INTO`.
- Crear la tabla `current_employees_silver` aplicando `UPPER()` a la columna `Role` y añadiendo marcas de tiempo de auditoría.
- Crear una vista temporal (temp view) utilizando una agregación con `GROUP BY`.
- Crear la tabla `total_roles_gold` y poblarla mediante `INSERT OVERWRITE`.
- Explorar el linaje, los permisos y la información detallada (insights) en Catalog Explorer.
- Ponte a prueba — Notebook de práctica
- Construye tu propio pipeline Medallion aplicando transformaciones diferentes
- Crea por tu cuenta un pipeline completo (Bronze → Silver → Gold), pero con transformaciones distintas: convierte a mayúsculas la columna `Country` (en lugar de `Role`), añade un número de fila (row number) y crea una tabla Gold que cuente los empleados por país (en lugar de por rol).

## Lo que practicarás:
- Crear una tabla Bronze y cargar datos mediante `COPY INTO`.
- Transformar datos en la capa Silver utilizando `UPPER()`, marcas de tiempo y `ROW_NUMBER()`.
- Crear una tabla de agregación Gold mediante `INSERT OVERWRITE`.
- Explorar el linaje en Catalog Explorer.

# Conclusión
Lo que has aprendido
- La arquitectura Medallion organiza los datos en capas: Bronze (datos sin procesar), Silver (datos depurados) y Gold (datos agregados).
- La ​​capa Bronze conserva los datos originales como red de seguridad; la capa Silver los estandariza y enriquece; la capa Gold responde a preguntas de negocio específicas.
- `INSERT OVERWRITE` permite actualizar las tablas Gold de forma programada.
- Unity Catalog rastrea automáticamente el linaje, los permisos y la actividad de las consultas en todas las capas.