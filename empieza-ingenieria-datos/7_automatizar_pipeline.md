# Seguimiento — Notebook de demostración
Crear y ejecutar un trabajo (Job) de LakeFlow en la interfaz de usuario
El notebook de demostración proporciona el contexto, pero esta lección se desarrolla principalmente en la interfaz de usuario de «Jobs & Pipelines» (Trabajos y Pipelines). Creará un nuevo trabajo, añadirá dos notebooks como tareas (tasks) con una dependencia entre ellos y ejecutará el trabajo para observar cómo se procesa el pipeline de forma automática.

## Lo que hará:
- Acceder a «Jobs & Pipelines» y crear un nuevo trabajo (Job)
- Añadir la Tarea 1 («Setup-Bronze»), vinculándola al notebook correspondiente a la capa Bronze
- Añadir la Tarea 2 («Silver-Gold»), estableciendo una dependencia con la Tarea 1
- Explorar las opciones de programación (scheduling) y activación (triggers)
- Hacer clic en «Run Now» (Ejecutar ahora) y observar cómo se ejecutan ambas tareas en orden
- Revisar el resultado de la ejecución completada
- Práctica — Notebook de ejercicios
- Verificar los resultados del pipeline automatizado
- Tras ejecutar el trabajo de LakeFlow, abra el notebook de ejercicios para comprobar las tablas que se han creado. Realice consultas (queries) sobre estas tablas generadas por el trabajo y compárelas con las tablas que creó manualmente en la Lección 6.

## Lo que practicará:
- Consultar las tablas de las capas Bronze, Silver y Gold creadas por el trabajo (con el sufijo «_job»)
- Comparar los resultados automatizados con las tablas creadas manualmente
- Comprender que la automatización genera el mismo resultado que la ejecución manual

# Conclusión
Lo que ha aprendido
- Los trabajos (Jobs) de LakeFlow permiten ejecutar uno o más notebooks como tareas, con dependencias configurables
- Las dependencias entre tareas garantizan que los pasos posteriores solo se ejecuten cuando los pasos previos hayan finalizado correctamente
- Los trabajos pueden activarse según una programación, ante la llegada de un archivo o de forma manual
- La automatización produce los mismos resultados en el pipeline sin necesidad de intervención manual