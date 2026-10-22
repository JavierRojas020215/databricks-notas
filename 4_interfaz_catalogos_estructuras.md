# Introducción
Este recorrido guiado le presenta el Explorador del catálogo, que es la interfaz de usuario principal para interactuar con Unity Catalog en un espacio de trabajo.

## Catálogo y espacio de nombres de tres niveles.
Para acceder al Explorador de catálogos, haga clic en Catálogo en la barra lateral de navegación. Databricks utiliza un espacio de nombres de tres niveles para organizar y administrar activos de datos. Para hacer referencia a activos de datos dentro del código, deberá utilizar la siguiente estructura de referencia: catalog.schema.data-object. El catálogo es el contenedor de nivel superior. Los esquemas son contenedores lógicos bajo el catálogo. Los esquemas pueden contener tablas, volúmenes, modelos y funciones almacenadas.

## Navegar por el Explorador del catálogo
El Explorador del catálogo utiliza una navegación de tipo árbol para acceder a los diferentes catálogos y a los esquemas y activos de datos subyacentes. Si un esquema contiene más de un tipo de activo de datos, se separarán por tipo en el árbol de navegación. En otros entornos, los esquemas se conocen como bases de datos, pero en Databricks contienen algo más que conjuntos de datos. Los catálogos tienen al menos dos esquemas estándar, default e information_schema. Default es un esquema inicial vacío que puede usar cuando se crea el catálogo, e information_schema contiene vistas de metadatos de los objetos del catálogo.

## Fichas de catálogo
La vista Catálogo tiene las siguientes pestañas:
Descripción general: incluye una descripción del catálogo y una lista de esquemas incluidos. Puede utilizar IA para generar descripciones detalladas de un catálogo para acelerar la anotación de sus catálogos.
- Detalles: muestra metadatos técnicos sobre el catálogo.
- Permisos: otorgar o revocar permisos a nivel de catálogo
- Políticas: adjunte filtros de fila o columna a nivel de catálogo que se heredarán en los esquemas y objetos de datos siguientes
- Espacios de trabajo: una lista de espacios de trabajo en los que se incluye este catálogo.

## Pestañas de esquema
La vista Esquema tiene las siguientes pestañas:
- Descripción general: incluye una descripción del esquema y una vista de las tablas, volúmenes, modelos y funciones dentro del esquema.
- Detalles: muestra metadatos técnicos relacionados con el esquema.
- Permisos: permite conceder o revocar permisos a nivel de esquema.
- Directivas (Policies): permite aplicar filtros de fila o columna a nivel de esquema, los cuales serán heredados por los objetos de datos contenidos en dicho esquema.

## Pestañas de tabla
La vista de tabla incluye las siguientes pestañas:
- Información general (Overview): contiene una descripción y una lista de las columnas de la tabla. Es posible utilizar IA para añadir una descripción y comentarios a las columnas; también se pueden asignar etiquetas a las columnas.
- Datos de muestra (Sample Data): ejecuta una consulta sencilla (`SELECT * FROM nombre_de_la_tabla`) para previsualizar los datos contenidos en la tabla.
- Detalles: muestra metadatos técnicos de la tabla, como el propietario y el tipo de datos, además de indicar si la tabla está gestionada (managed).
- Permisos: permite conceder o revocar permisos a nivel de tabla.
- Directivas (Policies): permite aplicar filtros de fila o columna a nivel de tabla, los cuales enmascararán los datos según los permisos de cada usuario o grupo.
- Historial (History): registro de auditoría de todos los cambios y ediciones realizados en la tabla.
- Linaje (Lineage): muestra las dependencias ascendentes y descendentes de la tabla; puede visualizarse en formato de tabla o de gráfico.
- Información detallada (Insights): ofrece datos sobre el uso, como los lugares donde se utiliza la tabla con mayor frecuencia y qué usuarios acceden a ella más a menudo.
- Calidad (Quality): si la supervisión de la calidad está habilitada, muestra información sobre la actualidad (frescura) y la integridad de los datos, así como detalles sobre posibles anomalías en el conjunto de datos.

## Configuración de permisos
Desde la pestaña de permisos, es posible conceder o revocar permisos a otros usuarios sobre activos y objetos de datos, tales como catálogos, esquemas y tablas. La interfaz de usuario permite asignar estos permisos de forma sencilla mediante clics y selecciones. Para que los usuarios o grupos puedan acceder a un activo de datos (ya sea para visualizarlo, utilizarlo o editarlo), deben contar también con permisos de uso (`USE`) en el esquema y el catálogo principales dentro de la jerarquía. La interfaz de usuario advierte sobre este requisito al intentar conceder permisos que dependen de privilegios en niveles superiores.

# Conclusión
En esta lección, has aprendido a:
- Acceder al Explorador de catálogos (Catalog Explorer) en la interfaz de usuario del espacio de trabajo de Databricks.
- Reconocer el espacio de nombres de tres niveles utilizado para hacer referencia a objetos de datos en toda la plataforma.
- Navegar por las opciones de la interfaz de usuario correspondientes a catálogos, esquemas y tablas. Establece permisos en los activos de datos mediante la interfaz de usuario de Catalog Explorer.
- Identifica cuándo se requieren permisos adicionales en niveles anteriores (upstream) para acceder adecuadamente a un objeto de datos.