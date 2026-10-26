# Sigue el proceso: Cuaderno de demostración
Viaja en el tiempo a través de la tabla `employees`
El cuaderno de demostración te muestra cómo inspeccionar el historial de versiones a partir de los cambios realizados en la Lección 2 y cómo consultar versiones anteriores específicas. Compararás el estado actual con instantáneas (snapshots) previas y verás cómo la función de «viaje en el tiempo» (time travel) te permite recuperarte de errores.

## Lo que harás:
- Ejecutar `DESCRIBE HISTORY` para ver todas las versiones y las operaciones realizadas en ellas.
- Consultar la tabla original mediante `VERSION AS OF 0`.
- Consultar el estado posterior a la operación `INSERT` mediante `VERSION AS OF 1`.
- Comparar el número de filas entre distintas versiones utilizando `UNION ALL`.
- Emplear la sintaxis abreviada `@v0`.

## Pruébalo: Cuaderno de ejercicios
- Explora el historial de versiones de `new_employees`
- Utiliza la función de «viaje en el tiempo» en la tabla `new_employees` para explorar los cambios que realizaste en el 

## Ejercicio 2. Asocia cada versión con la operación que la generó y compara los datos entre las distintas versiones.
Requisito previo: Debes completar el Ejercicio 1 y el Ejercicio 2 antes de comenzar este ejercicio.
Lo que practicarás:
- Visualizar el historial de versiones mediante `DESCRIBE HISTORY`.
- Consultar versiones específicas mediante `VERSION AS OF`.
- Comparar el número de filas entre la versión actual y las versiones anteriores.
- Utilizar la sintaxis abreviada `@v`.

# Conclusión
Lo que has aprendido
- Consultar el registro completo de cambios mediante `DESCRIBE HISTORY`.
- Consultar cualquier versión anterior utilizando `VERSION AS OF` o la sintaxis abreviada `@v`.
- Comparar datos entre versiones para comprender qué ha cambiado.
- Cada cambio queda registrado: nada se pierde realmente.