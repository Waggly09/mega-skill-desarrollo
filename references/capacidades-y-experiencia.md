# Capacidades y experiencia de Savia

Para una capacidad nueva, parte de `docs/product/industrial-enterprise-operating-system.md` y `docs/ux/role-adaptive-experience.md`. Identifica qué evento inicia el trabajo, quién toma la decisión, de dónde viene cada dato y quién consume la evidencia. Antes de añadir un módulo, comprueba si el registro de arquitectura, la configuración por planta o un módulo existente ya resuelven parte del proceso.

| Área | Entrada para localizar el flujo |
| --- | --- |
| Operación industrial, mantenimiento, inocuidad y seguridad operativa | Dominio correspondiente en `services/api/app/` y contrato de proceso en `docs/product/`. |
| Calidad, documentos y gobierno | Sigue el registro fuente, su evidencia y su estado en los dominios de control documental, cumplimiento y gobierno. |
| Capacitación y constancias | `services/api/app/learning/` y `docs/product/human-resources-learning.md`. Verifica qué material o evaluación habilita la emisión y qué tipo de constancia corresponde. |
| Salud ocupacional, personal y TI | Parte del dominio que posee el registro. Verifica qué información puede consultar el puesto y qué datos salen de ese dominio. |
| Web, móvil y escritorio | `apps/web/` comparte la experiencia de aplicación. `desktop/` cubre la integración específica de Electron. |

- Para una pantalla nueva, respeta la navegación por puesto, la planta activa y el patrón del módulo. Muestra qué falta para tomar una decisión y dónde abrir la evidencia. Comprueba el flujo completo con teclado y en el tamaño de pantalla del puesto. En un diálogo largo, verifica que se pueda llegar a la acción de guardar sin perder el contexto.
- Reutiliza `apiRequest` cuando aplique el contrato web vigente. Conserva paginación y estados de carga, vacío, error y denegación. Los indicadores deben identificar su periodo, filtros, unidad, fuente y cobertura. Un registro faltante y un valor de cero requieren estados distintos.
- Mantén los códigos técnicos persistidos y usa la localización de la interfaz para el español de México. Comprueba la regla de fecha del dominio antes de convertir zonas horarias, en especial cuando un valor representa un día civil.
- Para una integración o un asistente, identifica quién tiene autoridad sobre los datos, qué acceso permite el contrato y dónde entra la revisión humana. Distingue una salida de prueba, una lectura real y una acción habilitada. Si se menciona un estándar o requisito, identifica fuente, versión, alcance y validación competente antes de declararlo cubierto.
