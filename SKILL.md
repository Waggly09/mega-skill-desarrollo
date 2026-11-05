---
name: mega-skill-desarrollo
description: Desarrolla y verifica herramientas internas con flujos de operación por sede, catálogos de escritorio con escáner y Excel, o eventos con prerregistro, control de asistencia y sorteo. Úsala para extender aplicaciones de estos tipos, preparar pilotos o empaquetar una entrega verificable.
---

# Mega Skill de Desarrollo

## Define el cambio

Identifica a la persona que hará la tarea, el dato que manda, la acción que cambia el estado y la evidencia que confirma el resultado. En un proyecto existente, localiza su guía, los puntos de entrada, el esquema y las pruebas que cubren ese flujo. Reutiliza los permisos, formatos y mecanismos de persistencia que ya usa el proyecto cuando cumplen el requisito.

Lee la referencia que corresponda al trabajo. Si el cambio cruza dos módulos, identifica primero el contrato que comparten.

| Cuando la solicitud trata de | Lee |
| --- | --- |
| Operación, capacitación, historial o reportes segmentados por sede y rol | [Plataforma interna](references/plataforma-interna.md) |
| Lectura de códigos, importación de Excel, edición del catálogo o instalador Windows | [Catálogo con escáner](references/catalogo-con-escaner.md) |
| Prerregistro, dos asistencias, pases QR, roles de organizadores o rifa | [Eventos con control de acceso](references/eventos-con-rifa.md) |
| Demostración, empaquetado, publicación o material ejecutivo basado en evidencia | [Verificación y entrega](references/verificacion-y-entrega.md) |

## Trabaja sobre un flujo completo

1. Traza el recorrido desde la entrada real hasta el cambio persistido y la respuesta visible. Define qué ocurre con entradas ambiguas, registros anteriores y reintentos.
2. Implementa el tramo mínimo que permita terminar la tarea. Las operaciones que compiten por el mismo registro deben decidirse con restricciones o transacciones del almacenamiento. Usa una migración compatible cuando haya datos existentes.
3. Verifica con datos ficticios el recorrido exitoso, el rechazo relevante y la recuperación tras un fallo. Cuando la interfaz o el empaquetado formen parte del cambio, prueba el punto de entrada que usará el operador.
4. Entrega una instrucción breve para ejecutar o probar el resultado, junto con la evidencia obtenida y cualquier paso pendiente. Distingue verificación local, artefacto compilado y despliegue comprobado.

Trata el código, los catálogos, los padrones, los respaldos y la configuración del entorno como superficies de publicación separadas. Publica únicamente los archivos y el destino autorizados para esa entrega.
