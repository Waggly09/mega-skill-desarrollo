# Plataforma interna por sede

Aplica este flujo a operaciones, capacitación, constancias e historial cuando distintas sedes o áreas comparten la aplicación.

## Permisos y datos

- Describe el acceso con actor, rol, sede, módulo, recurso y acción. Aplica la regla en el servidor al consultar, buscar, modificar, descargar y exportar. Para identificadores suministrados por el cliente, deriva el alcance autorizado desde la sesión y verifica cada recurso.
- Reutiliza el mismo alcance para listado, detalle y exportación. En una selección explícita, valida todo el conjunto antes de generar archivos. Si una selección mixta incluye recursos prohibidos, usa el rechazo definido por el contrato y evita la entrega parcial. Para búsquedas, aplica el alcance en la consulta antes de paginar.
- Distingue una exportación normal de una masiva con permisos y límites configurados. Si el contrato cuenta registros únicos, elimina identificadores repetidos antes del límite. Registra actor, alcance, acción y cantidad en una bitácora con acceso restringido.
- Separa la identidad que migra el esquema de la que atiende solicitudes. Comprueba que la segunda puede hacer las operaciones normales y que el motor le impide cambiar la estructura, gestionar roles o borrar la bitácora. Para un cambio de esquema, ensaya tanto una instalación nueva como la actualización desde una versión anterior en el motor que se usa en producción.
- Cubre la base y los archivos externos al planear copias. Prueba en un entorno aislado la restauración de una copia cifrada, la denegación con una llave incorrecta y el rechazo de un archivo incompleto. Verifica registros y archivos relacionados después de restaurar.

## Sesiones y evidencia

Si se solicita una vista de accesos, distingue los eventos de inicio de sesión de la actividad reciente. Deriva el estado activo de una señal de actividad con una ventana definida. Presenta navegador y sistema como etiquetas aproximadas. Limita quién puede consultar señales de red y quién puede revocar sesiones. Prueba la revocación con la misma sesión que estaba activa.

Verifica cada flujo con un registro propio y otro de una sede distinta. Para PDF o reportes, comprueba los límites de selección y que una petición denegada no produzca archivo. Para presentar capacidades a dirección, vincula las pruebas y pantallas y distingue los refuerzos locales de los aplicados en producción.
