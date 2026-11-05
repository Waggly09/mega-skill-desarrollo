---
name: mega-skill-desarrollo
description: Organiza, diseña y desarrolla sistemas internos para operación industrial. Úsala al iniciar o ampliar una plataforma con módulos de producción, calidad, inventario o mantenimiento que comparten registros, permisos por planta y trazabilidad.
---

# Mega Skill de Desarrollo Industrial

## Elige el punto de partida

- **Sistema nuevo.** Delimita un proceso real y un primer piloto. Mapea los módulos, quién es responsable de cada registro y los traspasos entre áreas. Ordena el trabajo por recorridos que se puedan usar y verificar de principio a fin.
- **Sistema existente.** Localiza sus instrucciones, los puntos de entrada, los contratos y las pruebas del flujo. Identifica cómo están organizados los datos y quién los consume antes de proponer nuevos módulos, tablas o servicios.
- **Planificación o diagnóstico.** Entrega el mapa actual o propuesto, las dependencias, las decisiones abiertas y un backlog con criterios verificables. Inicia la implementación cuando forme parte de la solicitud.

| Si la tarea trata de | Abre esta referencia |
| --- | --- |
| Alcance, mapa de módulos, arquitectura, roadmap o primer piloto | [Organización y arquitectura](references/organizacion-y-arquitectura.md) |
| Nuevo módulo, tablero, flujo por puesto, navegador, móvil o escritorio | [Capacidades y experiencia](references/capacidades-y-experiencia.md) |
| Producción, captura, formatos, aprobaciones, historial o trazabilidad | [Operación y trazabilidad](references/operacion-y-trazabilidad.md) |
| Usuarios, sesiones, alcance por planta, expedientes, descargas o respaldo | [Acceso y datos](references/acceso-y-datos.md) |
| Pruebas, migraciones, liberación o validación de un piloto | [Verificación y entrega](references/verificacion-y-entrega.md) |

## Cierra el recorrido

1. Define el puesto que actúa, su ámbito, la decisión, el dato de origen y la evidencia que queda. Sigue el flujo desde la entrada real hasta la persistencia y el resultado visible para el siguiente puesto.
2. Define los estados, transiciones, permisos y comportamiento ante reintentos que afectan el flujo. Usa los contratos y la configuración existentes. Para un diseño nuevo, elige las herramientas según el entorno de operación, las integraciones y la capacidad del equipo para mantenerlas.
3. Implementa y verifica el menor recorrido que complete la tarea. Incluye datos sintéticos para el caso normal y los rechazos relevantes. Cuando se escriben registros, comprueba el reintento, la reapertura y la convivencia con datos anteriores.
4. Entrega el cambio o plan con su evidencia, decisiones pendientes y criterios para el siguiente paso. Distingue lo planeado, lo probado en desarrollo y lo validado en operación.
