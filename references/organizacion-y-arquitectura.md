# Organización y arquitectura

## Mapea el trabajo

1. Describe el recorrido en términos del personal de planta. Anota qué lo inicia, qué áreas intervienen, dónde se decide y cómo se corrige un error. Usa un caso real anonimizado o uno sintético que conserve las excepciones relevantes.
2. Agrupa capacidades por responsabilidad y reglas de negocio. Asigna a cada registro un módulo dueño, un identificador estable y sus consumidores. Si dos áreas usan el mismo dato con propósitos distintos, acuerda quién lo publica y qué vista necesita cada una.
3. Distingue los catálogos compartidos, la configuración por planta y los registros de operación. Identifica qué reglas son comunes, cuáles varían y quién puede publicar cada cambio.
4. Documenta el contrato de cada traspaso con el origen, el estado requerido, los datos mínimos y la respuesta ante un rechazo o reintento.

## Elige una arquitectura que se pueda operar

En un proyecto existente, empieza con sus límites y convenciones. En uno nuevo, compara las opciones a partir de las transacciones que deben completarse juntas, el acceso desde piso, el volumen previsto, los sistemas externos y quién dará soporte. Una aplicación modular con un solo despliegue puede simplificar un piloto si el mismo equipo opera los módulos. Evalúa separar un componente cuando tenga una frontera concreta de disponibilidad, seguridad, escala o ciclo de despliegue. Registra la decisión, el motivo y qué evidencia justificaría revisarla.

Coloca las transiciones del negocio en el módulo que posee el registro. Publica contratos para que otros módulos consulten o soliciten cambios. Mantén localizadas las integraciones externas, con reglas para errores, reintentos y conciliación de lo recibido. Para reportes transversales, conserva un vínculo a los registros de origen.

## Organiza el backlog por recorridos

Usa una ficha por capacidad. Enlaza las fichas con las decisiones de arquitectura y las pruebas que confirman cada entrega.

| Campo | Qué registrar |
| --- | --- |
| Puesto y objetivo | Quién actúa, en qué planta y qué resultado necesita. |
| Registro y dueño | Qué registro cambia, quién lo gobierna y quién lo consulta. |
| Estados y excepciones | Qué habilita la transición y qué pasa ante una corrección o un reintento. |
| Acceso y evidencia | Quién puede consultar, actuar o aprobar y qué queda registrado. |
| Dependencias | Catálogos, permisos, integraciones y decisiones pendientes. |
| Aceptación | Resultado observable, caso de rechazo y condición para validar el piloto. |

Prioriza por impacto operativo, dependencias y riesgo. Define primero lo mínimo de catálogos y acceso que habilite el recorrido piloto. Divide la entrega en tramos que se puedan demostrar con los puestos reales. Amplía módulos o plantas después de observar cómo se usa el primer flujo y qué excepciones aparecen.

## Ejemplo ficticio de un piloto

Recepción registra un lote y conserva su origen. Calidad inspecciona ese lote y emite un dictamen. Almacén registra la entrada con base en el dictamen autorizado. Cada módulo posee su registro y comparte el identificador de lote.

El piloto cubre el catálogo mínimo de materiales, tres perfiles en una planta, las tres transiciones y un historial consultable. Los criterios incluyen bloquear la entrada de un lote rechazado, impedir que otro ámbito acceda al lote y conservar un único movimiento si se repite la misma solicitud. La conexión con un sistema externo se planifica a partir del contrato y la conciliación del flujo validado.
