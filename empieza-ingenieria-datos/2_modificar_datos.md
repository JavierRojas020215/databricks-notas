# Sigue el proceso: Cuaderno de demostración
## Modifica la tabla `employees` paso a paso
El cuaderno de demostración te guía a través de tres tipos de modificaciones en la tabla `employees`. Añadirás nuevos empleados, actualizarás un puesto, eliminarás un registro y revisarás el historial de versiones después de cada cambio.

### Lo que harás:
- Insertar dos nuevos empleados (Maria y Aiden) mediante `INSERT INTO`.
- Actualizar el puesto de Maria mediante `UPDATE ... SET ... WHERE`.
- Eliminar el registro de Aiden mediante `DELETE FROM ... WHERE`.
- Consultar el registro completo de cambios mediante `DESCRIBE HISTORY`.
- ¡Pruébalo! — Cuaderno de ejercicios
- Modifica la tabla `new_employees` por tu cuenta
- Aplica las mismas operaciones `INSERT`, `UPDATE` y `DELETE` a la tabla `new_employees`. Añadirás un nuevo empleado, cambiarás un puesto y eliminarás un registro; después, comprobarás el historial de versiones.

### Lo que practicarás:
- Insertar una fila con valores específicos.
- Actualizar el valor de una columna mediante una cláusula `WHERE`.
- Eliminar una fila a partir de un nombre.
- Confirmar que todas las operaciones quedan registradas en el historial mediante `DESCRIBE HISTORY`.

# Conclusión
Lo que has aprendido
- Añadir filas a una tabla mediante `INSERT INTO`.
- Modificar valores mediante `UPDATE ... SET ... WHERE`.
- Eliminar filas mediante `DELETE FROM ... WHERE`.
Cada operación DML crea una nueva versión que es registrada por Delta Lake.