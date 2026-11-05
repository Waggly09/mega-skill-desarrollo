# Operación y trazabilidad

Sigue una orden, lote, activo o expediente a través de sus etapas. Para cada traspaso, identifica la relación que permite volver al origen. Si un lote se divide o se combina, conserva las relaciones y cantidades necesarias para seguir el recorrido en ambas direcciones.

## Captura y transición

- Define qué fuente tiene autoridad sobre cada valor. Para mediciones, conserva unidad, momento de captura y procedencia. Si un dato viene de una fuente industrial, respeta el contrato de calidad y procedencia del dominio.
- En formularios configurables, carga la versión publicada que corresponda a la planta, módulo y actividad. Valida en el servidor la versión, los campos, los tipos y las opciones. Guarda la versión exacta con la captura y comprueba que se pueda reabrir e imprimir después de publicar otra.
- En un traspaso entre etapas, conserva el vínculo con el registro anterior y comprueba si se requiere un estado previo. Si el mismo movimiento puede llegar dos veces, conserva una única consecuencia operativa y devuelve el resultado persistido conforme al contrato.
- Para correcciones y anulaciones, sigue la transición prevista en el dominio. Registra actor, fecha, motivo y vínculo con el original. Verifica los efectos en los registros dependientes y en la bitácora.

## Consulta y evidencia

- Para el historial compartido, consulta los registros desde el módulo que los gobierna o mediante una vista que conserve la referencia al origen. Distingue el historial operativo, la bitácora de cambios y la consulta transversal de trazabilidad.
- Aplica los filtros autorizados antes de paginar. Vincula anexos por su relación con el registro y respeta su alcance. Al imprimir varios registros, conserva su versión y renderizador. Si se solicita el diseño original, comprueba el PDF con la plantilla correspondiente.

Prueba una captura y su reapertura tras publicar un formato nuevo, un traspaso repetido, un registro excluido por planta y una búsqueda que supere una página cuando la colección sea paginada.
