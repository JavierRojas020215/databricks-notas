# Introducción
Este recorrido guiado le ayuda a crear y navegar por un notebook de Databricks, a comprender la disposición de su interfaz de usuario y a utilizar sus funciones principales, como las celdas, Markdown, el modo de enfoque y las visualizaciones.

## Crear y nombrar un notebook
Puede crear un notebook de tres formas:
-En el explorador del área de trabajo (Workspace), haga clic con el botón derecho en la carpeta donde desee añadir un notebook y seleccione «Create» (Crear) y, a continuación, «Notebook».
-Tras navegar hasta la carpeta donde desee añadir un notebook, haga clic en «Create» (Crear) en la parte superior derecha de la pantalla y seleccione «Notebook».
-Haga clic en «+ New» (Nuevo) en el menú de navegación y seleccione «Notebook». Esto creará un nuevo notebook en su carpeta de inicio predeterminada. Los notebooks nuevos tienen un nombre temporal; haga clic en el título, en la parte superior del notebook, para cambiarle el nombre. Una vez creado el notebook, puede utilizar el selector de recursos de computación (compute selector), situado en la parte superior derecha, para asociarlo a un clúster o a un SQL Warehouse. En la edición gratuita (Free Edition), la computación sin servidor (serverless compute) es la única opción disponible y se iniciará automáticamente al ejecutar una celda.

## Trabajar con celdas en un notebook
Entre las celdas, puede seleccionar «+ Code» (Código), «+ Text» (Texto) o «Assistant» (Asistente) para insertar una nueva celda. Las celdas de código pueden ejecutarse haciendo clic en el botón «Run» (Ejecutar) —representado por un icono de reproducción— situado en la esquina superior izquierda de la celda, o bien pulsando la combinación de teclas Shift + Enter. Cada notebook tiene un lenguaje predeterminado, que se indica en la parte superior, junto al menú de ayuda. Los notebooks de Databricks admiten Python y SQL. Las celdas nuevas se crean utilizando el lenguaje predeterminado, pero puede cambiar el lenguaje de cada celda de forma individual mediante el menú desplegable situado en la esquina superior derecha de la misma. Al cambiar el lenguaje de una celda, se añade un comando especial (conocido como «magic command»: %py, %sql o %md) en la parte superior de dicha celda. Si tiene habilitada la opción de pestañas para los notebooks en la configuración (Settings), cada notebook se abrirá en su propia pestaña, lo que le permitirá alternar entre varios notebooks sin tener que volver al explorador del área de trabajo. También puede reorganizar estas pestañas arrastrándolas y soltándolas.

## Markdown en los notebooks
Las celdas Markdown se utilizan para añadir documentación, como encabezados, listas con viñetas, enlaces y tablas. Para crear una celda de Markdown, puedes hacer clic en «+ Texto», cambiar el tipo de celda a «Markdown» mediante el selector de lenguaje o escribir «%md» al principio de la celda. Haz doble clic en una celda de Markdown para editarla y utiliza la opción «Mostrar vista previa» (Show Preview) para ver el resultado renderizado junto al texto que estás editando. Los encabezados de Markdown bien estructurados aparecen automáticamente en el panel «Tabla de contenido» (Table of Contents), situado a la izquierda del notebook; esto facilita la navegación por notebooks extensos, ya que basta con hacer clic en el encabezado correspondiente dentro de dicho panel.

## Opciones de las barras laterales izquierda y derecha
La barra lateral izquierda de navegación de un notebook incluye:
- Tabla de contenido (Table of Contents): la estructura de encabezados del notebook, basada en el contenido en formato Markdown.
- Icono de carpeta: abre el explorador del espacio de trabajo en un panel lateral, lo que permite navegar por otros notebooks y recursos almacenados en las carpetas de tu espacio de trabajo.
- Icono de catálogo: ofrece una vista compacta del Explorador de catálogos (Catalog Explorer), donde puedes explorar catálogos, esquemas, tablas y volúmenes. También puedes utilizarlo para insertar referencias directamente en tu código. La barra lateral derecha contiene accesos directos a: comentarios, experimentos de MLflow, historial de versiones, variables, entorno (relacionado con el entorno de computación), información y el asistente (Assistant). Estas herramientas te ayudan a añadir anotaciones, realizar un seguimiento de los experimentos e inspeccionar el estado del notebook mientras trabajas.

## Ejecución de código y visualización de resultados
Al ejecutar una celda de código, el resultado aparece justo debajo de la misma. En el caso de celdas que no utilizan el lenguaje predeterminado del notebook, recuerda incluir el comando mágico (magic command) correspondiente para garantizar que el entorno de ejecución procese la celda correctamente. Puedes ejecutar celdas individuales mediante el botón «Ejecutar» (Run) o la combinación de teclas «Shift + Enter»; también puedes usar la opción «Ejecutar todo» (Run All), disponible en la barra de herramientas del notebook, para ejecutar todas las celdas de forma secuencial, de arriba hacia abajo.

## Modo de enfoque (Focus mode)
El modo de enfoque amplía una celda específica y sus resultados para que ocupen toda el área de visualización del notebook, eliminando así las distracciones que podrían causar las celdas circundantes. El icono del modo de enfoque se encuentra en la esquina superior derecha de cada celda. Incluso en este modo, seguirás teniendo acceso a los comentarios, al asistente y al panel de la terminal. Además, puedes desplazarte entre distintas celdas sin salir del modo de enfoque utilizando las flechas derecha e izquierda situadas en la parte superior de la ventana. Haz clic de nuevo en el icono para salir del modo de enfoque y volver a la vista completa del notebook. Visualizaciones en notebooks

Tras ejecutar una celda que devuelve resultados en formato tabular, puedes hacer clic en el icono «+» situado junto a los resultados para crear una visualización directamente al lado de la salida. Es posible configurar el tipo de gráfico (por ejemplo, de barras, de dispersión o de líneas), definir los valores de los ejes X e Y, y guardar la visualización. Una vez guardada, puedes alternar entre la tabla de resultados y la visualización dentro de la misma celda.

# Conclusión
En esta lección has aprendido a:
- Crear y renombrar un notebook, así como asignarle recursos de computación.
- Insertar y ejecutar una celda de código utilizando diversos lenguajes.
- Emplear celdas de Markdown para documentar y navegar por el notebook.
- Explorar las opciones disponibles en las barras laterales izquierda y derecha de la interfaz del notebook.
- Utilizar el modo de enfoque (Focus mode) para concentrarte en una celda específica y sus resultados.
- Crear visualizaciones integradas a partir de la salida de una celda.