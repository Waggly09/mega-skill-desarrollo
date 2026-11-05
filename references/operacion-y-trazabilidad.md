# Operación y trazabilidad

Empieza por `docs/guides/orientacion-del-codigo.md`. Sigue el componente en `apps/web/`, el contrato HTTP en `services/api/app/` y la capa que guarda el cambio. Para capturas e historial, consulta `docs/product/module-specific-forms.md` y `docs/product/module-operational-history.md`. Para cambios de un proceso industrial, identifica en `docs/product/` su contrato y en las pruebas sus casos límite.

## Captura y transición

- Define qué fuente tiene autoridad sobre cada valor. Para mediciones, conserva unidad, momento de captura y procedencia. Si un dato viene de una fuente industrial, respeta el contrato de calidad y procedencia del dominio.
- En formularios configurables, carga la versión publicada para la planta, módulo y actividad. Valida en la API la versión, los campos, los tipos y las opciones. Guarda la versión exacta con la captura y comprueba que se pueda reabrir e imprimir después de publicar otra.
- En un traspaso entre etapas, conserva el vínculo con el registro anterior y comprueba si se requiere un estado previo. Si el mismo movimiento puede llegar dos veces, conserva una única consecuencia operativa y devuelve el resultado persistido conforme al contrato.
- Para correcciones y anulaciones, sigue la transición prevista en el dominio. Registra actor, fecha, motivo y vínculo con el original. Verifica los efectos en los registros dependientes y en la bitácora.

## Consulta y evidencia

- Para el historial compartido, lee los registros nativos desde su dominio. Distingue historial operativo, bitácora de cambios y consulta transversal de trazabilidad. Los dominios con historial especializado conservan su contrato y su alcance.
- Aplica los filtros autorizados antes de paginar. Vincula anexos por su relación con el registro y respeta su alcance. Al imprimir varios registros, conserva su versión y renderizador. Si se solicita el diseño original, comprueba el PDF con la plantilla correspondiente.

Prueba una captura y su reapertura tras publicar un formato nuevo, un traspaso repetido, un registro excluido por planta y una búsqueda que supere una página cuando la colección sea paginada.
