---
name: mega-skill-desarrollo
description: Desarrolla y verifica cambios en Savia, la plataforma industrial y empresarial. Úsala para extender sus módulos, formularios, trazabilidad, permisos, interfaces, integraciones y entregas, o para documentar sus capacidades con evidencia del repositorio.
---

# Mega Skill de Savia

## Ubica el cambio

Trabaja en el clon de desarrollo indicado por el `AGENTS.md` de Savia. Confirma la raíz, la rama y el estado de Git antes de editar. Lee la guía del repositorio y usa `savia context` cuando esté disponible. Si tienes solo esta skill, solicita el clon o los archivos relevantes antes de afirmar cómo funciona una capacidad. Para decisiones de producto o seguridad, la evidencia es el código, las pruebas y la configuración de la versión que vas a cambiar.

| Si la tarea trata de | Abre esta referencia |
| --- | --- |
| Nuevo módulo, tablero, flujo por puesto, navegador, móvil o Electron | [Capacidades y experiencia](references/capacidades-y-experiencia.md) |
| Producción, captura, formatos, aprobaciones, historial o trazabilidad | [Operación y trazabilidad](references/operacion-y-trazabilidad.md) |
| Usuarios, sesiones, alcance por planta, expedientes, descargas o respaldo | [Acceso y datos](references/acceso-y-datos.md) |
| Pruebas, migraciones, liberación, pilotos o presentación ejecutiva | [Verificación y entrega](references/verificacion-y-entrega.md) |

## Cierra el recorrido

1. Define el puesto que actúa, la planta y el módulo, la decisión, el registro que manda y la evidencia que queda. Traza la pantalla o acción real hasta la API y la persistencia. Usa las reglas de dominio y la configuración publicadas que ya aplican a ese flujo.
2. Implementa el tramo mínimo completo. Si cambias un contrato, verifica los consumidores y los registros que ya existen. Mantén los permisos en el servidor y preserva la procedencia, versión y alcance de los datos. Deja que el almacenamiento resuelva las escrituras concurrentes que compiten por el mismo recurso.
3. Verifica con datos sintéticos el camino permitido, el rechazo relevante y el reintento o reapertura cuando haya escrituras. Ejecuta las pruebas focalizadas y `git diff --check`. Sigue el alcance de verificación que marque el repositorio para el tipo de cambio.
4. Reporta el efecto para el puesto, la evidencia de prueba y el paso pendiente de validación o promoción, si existe. Un resultado de desarrollo sustenta esa versión y ese entorno.

Las rutas de código y documentos que nombran las referencias son relativas al clon de Savia. Compruébalas en la rama activa. Las skills locales de Savia y su `AGENTS.md` rigen el trabajo en ese clon.
