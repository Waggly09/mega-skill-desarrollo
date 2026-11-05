# Verificación y entrega

## Reproduce la operación

- Prepara datos sintéticos con las mismas formas y casos límite que los datos reales. Usa un perfil local con su propia base y configuración. Si existe una demo, comprueba que sus usuarios y registros queden aislados del entorno real.
- Registra el entorno, el comando, el resultado y la evidencia que viste. Cuando un servicio, un dispositivo o un destino no estén disponibles, marca el caso como pendiente de comprobar.
- Prueba la tarea con el dispositivo y perfil que usará la persona. Para un lector, ejecuta el recorrido de escaneo y Enter. Para un evento, usa un teléfono para el registro público y una cuenta de acceso para confirmar la entrada. Para una plataforma interna, combina un perfil autorizado con otro que deba recibir una denegación.

## Empaqueta y publica

1. Crea la entrega a partir de una lista explícita de archivos. Incluye las instrucciones de arranque y una plantilla de configuración con valores ficticios. Usa un catálogo vacío o un conjunto de demostración generado.
2. Inspecciona el contenido de archivos comprimidos e instaladores y, cuando haya Git, revisa también el árbol y el historial que vas a subir. Busca credenciales, rutas privadas, inventarios, identificadores de personas, exportaciones, bases, respaldos y archivos de entorno. Un archivo ignorado puede seguir presente en commits anteriores.
3. Reproduce la instalación o compilación desde la entrega con un perfil limpio. Comprueba el primer arranque, dónde quedan los datos y qué ocurre al aplicar una actualización. Para una aplicación web, comprueba desde fuera del entorno local que la URL sirve la versión esperada y que conserva el esquema y los permisos correctos.
4. Si se autorizó una publicación, confirma cuenta, repositorio y visibilidad. Verifica después la rama y el commit que quedaron publicados. Para una entrega pública, comprueba el acceso sin sesión.

## Documenta para decisión y operación

Separa lo comprobado, lo disponible con configuración adicional y lo que sigue en propuesta. Para cada capacidad importante, vincula la pantalla, código, prueba o configuración que la demuestra. Explica a quién beneficia y qué trabajo cambia. Cualquier cifra de ahorro, capacidad o adopción requiere una medición o una hipótesis identificada como tal.

Entrega a operación el procedimiento de primer uso, los permisos necesarios, el responsable de actualizar datos y los pasos de recuperación que sí se ensayaron. Si una parte de la entrega depende de una prueba física o de producción, identifica esa prueba y su resultado esperado.
