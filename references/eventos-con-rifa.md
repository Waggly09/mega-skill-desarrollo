# Eventos con prerregistro y rifa

Aplica cuando el acceso al sorteo depende de una actividad previa y de la presencia el día del evento.

## Separa los estados

| Acción | Evidencia y decisión |
| --- | --- |
| Prerregistro | Vincula al participante con una entrada del padrón sin mostrar si otras personas existen. Separa la intención de asistir de la asistencia a la actividad previa. |
| Confirmación previa | Registra quién validó la asistencia y cuándo. Limita la confirmación a la ventana y al personal autorizados. |
| Acceso al evento | Resuelve un pase opaco asociado al evento. Confirma presencialmente con el criterio de identidad acordado. Un segundo escaneo debe recuperar el estado anterior sin contar otra entrada. |
| Sorteo | Calcula la elegibilidad en el servidor a partir de los estados exigidos. Conserva una lista cerrada para la ronda junto con el orden de premios y las exclusiones aplicadas. |

Ofrece al participante un enlace apto para teléfono y un registro asistido. Separa el acceso del participante del acceso autenticado del equipo. Si hay contactos de emergencia, solicita solo los campos necesarios, limita quién los puede ver y mantenlos fuera del QR, la pantalla pública y los registros del sorteo.

## Controla quién opera

Usa permisos distintos para administración, validación de asistencia y sorteo según el evento. Aplica los permisos en el servidor. Si se habilitan cuentas propias, usa invitaciones de uso único con caducidad y comprueba que una baja o cambio de rol surta efecto sobre sesiones existentes. Prevé una corrección de asistencia que deje actor, motivo y hora.

## Ejecuta una rifa reproducible en sus efectos

1. Congela las listas de participantes elegibles y premios para la ronda. Si el orden de entrega también es aleatorio, elige y guarda ese orden con un generador seguro y selección uniforme.
2. Elige al ganador entre los participantes disponibles con aleatoriedad del servidor. Persiste ganador, premio, ronda y operador de forma atómica, con restricciones para evitar duplicados y una clave de operación para reintentos. El resultado que se anima en pantalla debe provenir del registro confirmado.
3. Si falla la conexión después del guardado, recupera el resultado por su clave antes de intentar otro sorteo. Si se anula una entrega, conserva el resultado original en el historial y aplica el procedimiento acordado para reasignar.

Prueba un pase prestado, un pase escaneado dos veces, alguien que solo asistió a una actividad, un operador sin permiso y dos solicitudes de sorteo simultáneas. Si usas un destino de hosting nuevo, verifica el registro anónimo y la persistencia compartida entre dispositivos. Una demo con almacenamiento local sirve para ensayar la interfaz.
