# Acceso y datos

Para cada flujo, documenta qué roles actúan, en qué plantas o áreas, sobre qué registros y con qué facultades. Distingue quién captura, quién aprueba y quién puede corregir cuando el proceso requiera responsabilidades separadas.

- Modela cada permiso como actor, rol, planta, área, módulo, recurso y acción, según las dimensiones del flujo. Deriva el alcance autorizado de la sesión y aplícalo en el servidor a listados, detalles, escrituras y descargas. La visibilidad en la interfaz ayuda a navegar. Valida la autorización también con solicitudes directas a la API.
- Para una selección de exportación, verifica todos los recursos antes de emitir el archivo y aplica los límites de selección del rol. Un recurso fuera de alcance se maneja con el rechazo definido por el contrato. Comprueba la auditoría de la exportación y conserva los detalles sensibles fuera de los registros de diagnóstico.
- Para datos personales o clínicos, limita el acceso por finalidad y conserva las fronteras del dominio. Cuando otro puesto necesite el resultado de una decisión, comprueba si basta un estado autorizado en lugar de devolver el expediente que la sustenta.
- Para sesiones, distingue la actividad reciente, el inicio de sesión, la renovación y la revocación. Si cambias el cierre de una sesión o un permiso, verifica que la credencial activa reciba la respuesta esperada en su siguiente solicitud.
- Define permisos de almacenamiento para la aplicación y las migraciones según el entorno. Verifica con una base aislada las operaciones permitidas, el bloqueo de cambios de esquema para la aplicación y la protección de la bitácora. Para recuperación, comprueba el respaldo de la base y de los archivos vinculados, la restauración y el rechazo de una copia incompleta.

Una prueba de acceso debe cubrir un registro autorizado, uno fuera de alcance y la misma acción por su punto de entrada real. Si el cambio es de descarga o reporte, incluye una selección que mezcle ambos registros.
