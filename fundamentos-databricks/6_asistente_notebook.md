# Introducción
Este recorrido guiado le muestra cómo usar Databricks Assistant para generar código, escribir SQL y diagnosticar errores directamente desde sus notebooks.

## Localizar al asistente en cuadernos
Hay varias formas de abrir el Asistente en una libreta:
- Haga clic en el ícono del Asistente en la barra lateral derecha para abrir el panel de chat junto a su computadora portátil.
- Utilice el botón Asistente en la barra de navegación superior para abrir también el panel lateral del chat.
- Haga clic en el botón Asistente en línea entre celdas para abrir el Asistente dentro de la nueva celda. El panel de chat de la barra lateral permanece abierto mientras trabaja, lo que le permite interactuar con el Asistente mientras escribe y ejecuta código.

## Escribiendo Python con asistente
Puede indicar al asistente que genere código Python describiendo lo que necesita en lenguaje natural. El asistente responde con un fragmento de código que puede insertar en una celda nueva o aceptar y ejecutar en un solo paso. Por ejemplo, puede pedirle al asistente: «haz el cómputo de la suma de los enteros del 1 al 10», y generará un pequeño fragmento de Python que puede ejecutar y verificar inmediatamente.

## Escriba SQL con Asistente
El asistente también puede generar consultas SQL sobre sus tablas existentes. Cuando el lenguaje predeterminado del notebook es Python, el asistente puede responder con PySpark SQL, a menos que se especifique lo contrario. Una buena práctica es incluir el lenguaje en la indicación. Por ejemplo, pídale: «Usa SQL para seleccionar las primeras 10 filas de mi tabla». El código generado debe estar escrito en el tipo de código correcto.

## Depuración con Asistente
Cuando falla una celda, la interfaz de usuario del notebook muestra una opción de Diagnóstico de error si el Asistente de corrección rápida está habilitado. Al hacer clic en el botón Diagnosticar error, se envía el código de error y el mensaje de error al Asistente que se abre en el panel lateral. Luego explorará el error y proporcionará una explicación de lo que cree que salió mal y proporcionará una solución sugerida. Desde el panel lateral del asistente, puede ejecutar el código sugerido para probarlo o editar la sugerencia si tiene contexto adicional. A veces, solucionar un problema revela otro, por lo que es posible que deba realizar más diagnósticos para resolver completamente todo el problema.

## Mejores prácticas para el uso del asistente
El asistente es una herramienta potente; sin embargo, ten en cuenta las siguientes mejores prácticas:
Revisa siempre el código y los resultados generados antes de utilizarlos en un entorno de producción o compartirlos con otras personas.

Sé específico en tus instrucciones (prompts), incluyendo nombres de tablas, columnas y el lenguaje deseado para obtener un resultado más preciso.

Si un error persiste, analiza el seguimiento de la pila (stack trace) completo junto con la explicación proporcionada por el asistente. Esta información combinada puede ayudarte a identificar con exactitud qué tabla, esquema o privilegio falta o es incorrecto. El asistente está integrado en toda la plataforma; por ello, a medida que explores, busca oportunidades donde pueda facilitar tu trabajo de desarrollo.

# Conclusión
En esta lección has aprendido a:
- Abrir e interactuar con Genie Code desde diversos puntos de acceso dentro de un notebook.
- Generar código en Python y SQL mediante instrucciones en lenguaje natural.
- Utilizar la función de diagnóstico de errores (Diagnose Error) para depurar celdas que presentan fallos.
- Aplicar mejores prácticas —como la especificación detallada de instrucciones y la revisión de código— al utilizar Genie Code.