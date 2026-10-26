# Sigue el proceso — Cuaderno de demostración
Creación de tablas mediante CTAS y la interfaz de carga (Upload UI)
El cuaderno de demostración te guía a través de dos métodos de ingesta, presentados uno al lado del otro. Primero, utilizarás CTAS con opciones de formato explícitas para crear una tabla «limpia», sin la columna `_rescued_data`. Luego, emplearás la interfaz de usuario de Catalog Explorer para cargar el mismo archivo CSV sin necesidad de escribir código.

## Lo que harás:
- Ejecutar una sentencia CTAS con `read_files` y opciones de formato explícitas (`header`, `inferSchema`).
- Seleccionar únicamente las cuatro columnas de datos para obtener un esquema limpio.
- Utilizar la interfaz de carga de Catalog Explorer para crear una tabla mediante la función de arrastrar y soltar (drag-and-drop).
- Ejecutar `SHOW TABLES` para confirmar que ambas tablas existen.
- Pruébalo — Cuaderno de ejercicios

## Crea tu propia tabla mediante CTAS
Utiliza CTAS con opciones de formato explícitas para crear una tabla llamada `new_hires_ctas` a partir del archivo `employees2.csv`. Compara el número de columnas entre tu nueva tabla y la tabla `employees` de la Lección 1.

### Lo que practicarás:
- Redactar una sentencia CTAS con opciones de formato.
- Seleccionar columnas específicas de un archivo CSV.
- Comparar los esquemas de diferentes tablas utilizando `information_schema`.

# Conclusión
Lo que has aprendido
- Crear tablas mediante CTAS y opciones de formato explícitas para obtener esquemas limpios.
- Utilizar la interfaz de carga de Catalog Explorer para realizar una ingesta sin necesidad de código.
- CTAS ​​está diseñado para procesos (pipelines) y reproducibilidad; la interfaz de carga (Upload UI) es ideal para importaciones rápidas y puntuales (ad hoc).
- `SHOW TABLES` permite listar todas las tablas presentes en el esquema actual.