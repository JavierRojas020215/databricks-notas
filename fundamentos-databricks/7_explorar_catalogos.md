# Introducción
Este recorrido guiado le muestra cómo interactuar con Unity Catalog desde un notebook mediante SQL. Aprenderá a verificar el contexto actual, explorar esquemas, tablas y volúmenes, y conceder permisos de forma programática.

## Verificación y configuración del catálogo y el esquema actuales
El uso de `SELECT current_catalog(), current_schema();` le permite confirmar qué catálogo y esquema está utilizando actualmente su notebook. Esto resulta especialmente útil en notebooks extensos, donde es posible que haya perdido la referencia del contexto activo. Puede modificar el contexto mediante las sentencias `USE CATALOG` y `USE SCHEMA`. Conocer el contexto actual le permite determinar si es necesario especificar el nombre completo de las tablas o si puede recurrir a los valores predeterminados.

## Exploración del esquema
Para consultar los detalles de un esquema de manera programática, puede utilizar `DESCRIBE SCHEMA EXTENDED current_schema();`. El resultado muestra propiedades como el propietario del esquema, la ubicación de almacenamiento y cualquier comentario o propiedad personalizada que se haya definido, ofreciéndole una visión general rápida de la configuración del esquema.

## Exploración de tablas y vistas
Utilice `SHOW TABLES;` para listar todas las tablas y vistas presentes en el esquema actual. El resultado incluye el nombre, el tipo y los comentarios de cada tabla, lo que le ayudará a identificar los elementos disponibles para su uso. Las vistas aparecen junto a las tablas; es importante tener esto en cuenta al analizar las dependencias entre objetos o al determinar si un elemento puede editarse.

## Exploración de volúmenes
Ejecute `SHOW VOLUMES;` para listar todos los volúmenes lógicos registrados en el catálogo y esquema actuales, incluyendo sus nombres y ubicaciones de almacenamiento. Para un volumen específico, puede ejecutar un comando que liste todos los archivos contenidos en su ruta, permitiéndole identificar qué archivos sin procesar (raw files) están disponibles para su ingesta o procesamiento.

## Concesión de permisos desde un notebook
Unity Catalog emplea sentencias `GRANT` (conforme al estándar ANSI) para gestionar permisos directamente desde un notebook. Por ejemplo, puede conceder el permiso `SELECT` sobre una tabla a todos los usuarios de la cuenta mediante una única sentencia SQL. Unity Catalog aplica un modelo de privilegios jerárquico: para realizar consultas sobre una tabla, los usuarios también deben contar con los privilegios `USE CATALOG` y `USE SCHEMA` sobre los contenedores principales (catálogo y esquema). Puedes verificar tus permisos (grants) ejecutando `SHOW GRANTS` o consultando la pestaña «Permisos» (Permissions) en el Explorador de catálogos (Catalog Explorer). El enfoque recomendado consiste en utilizar SQL en los notebooks para automatizar los cambios de permisos cuando sea necesario, y emplear el Explorador de catálogos para confirmar visualmente que se han aplicado correctamente.

# Conclusión
En esta lección has aprendido a:
- Consultar y establecer el contexto actual de catálogo y esquema para un notebook.
- Utilizar SQL para explorar esquemas, tablas, vistas y volúmenes en Unity Catalog.
- Conceder permisos sobre activos de datos mediante programación, utilizando sentencias `GRANT`.
- Verificar los permisos tanto mediante SQL como a través de la interfaz de usuario del Explorador de catálogos.
- Explicar el modelo jerárquico de privilegios y los requisitos de permisos en niveles superiores (upstream) que aplica Unity Catalog.