# Seguimiento — Notebook de demostración
Revisa las definiciones del pipeline y crea un pipeline ETL
El notebook de la lección contiene tres sentencias SQL que definen el pipeline completo; sin embargo, a diferencia de otras lecciones, no ejecutarás las celdas de forma interactiva. En su lugar, revisarás las definiciones y, posteriormente, configurarás un pipeline ETL en la interfaz de usuario de «Jobs & Pipelines» (Trabajos y Pipelines), el cual apuntará a este notebook y lo ejecutará automáticamente.

## Lo que harás:
- Leer las tres definiciones de pipeline en SQL (tabla de streaming para la capa Bronze, vistas materializadas para las capas Silver y Gold).
- Comprender las expectativas de calidad de los datos mediante la cláusula `CONSTRAINT ... EXPECT` en la capa Silver.
- Acceder a «Jobs & Pipelines» y crear un nuevo pipeline ETL.
- Vincularlo al notebook de la lección y establecer el catálogo y el esquema de destino.
- Iniciar el pipeline y observar la ejecución del grafo acíclico dirigido (DAG) de tres nodos.
- Hacer clic en el nodo Silver para ver los resultados de las expectativas de calidad de los datos.
- Práctica — Notebook de ejercicios
- Explora los resultados de tu pipeline declarativo
- Una vez finalizado el pipeline ETL, abre el notebook de ejercicios para realizar consultas sobre las tablas creadas mediante SDP, compáralas con las tablas que construiste manualmente, y explora las expectativas de calidad de los datos y el linaje en el «Catalog Explorer» (Explorador de catálogos).
- Requisito previo: Debes completar la lección adicional (crear y ejecutar el pipeline ETL) antes de comenzar esta práctica.

## Lo que practicarás:
- Consultar las tres tablas creadas mediante SDP (con el sufijo `_sdp`).
- Comparar los resultados de la capa Gold generados por SDP con los resultados de la capa Gold creados manualmente.
- Explorar las expectativas de calidad de los datos en el «Catalog Explorer».
- Rastrear el linaje desde los archivos de origen a través de las capas Bronze, Silver y Gold.

# Conclusión
Lo que has aprendido
- Spark Declarative Pipelines (SDP) permite definir tablas de forma declarativa, evitando la necesidad de escribir una orquestación paso a paso.
- Las tablas de streaming gestionan la ingesta incremental, mientras que las vistas materializadas se encargan de las transformaciones y agregaciones.
- La cláusula `CONSTRAINT ... EXPECT` añade un seguimiento de la calidad de los datos a tu pipeline.
- SDP determina automáticamente el orden de ejecución, gestiona los recursos de cómputo y realiza un seguimiento del linaje.
- Obtienes los mismos resultados que en las lecciones 6 y 7, pero con menos código y una orquestación automatizada.