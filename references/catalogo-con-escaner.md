# Catálogo con escáner y Excel

Aplica a una aplicación de escritorio que identifica productos por código y permite mantener el catálogo.

## Importa sin perder identidad

- Lee los códigos como cadenas, de longitud variable. Si el libro define el código como la concatenación de dos columnas, concatena en el orden declarado en todas las hojas de origen. Conserva ceros iniciales y retira solo los separadores acordados. Si una celda numérica perdió dígitos y el formato no permite recuperarlos con certeza, reporta hoja y fila para corregir el origen.
- Usa la coincidencia exacta como primera regla. Solo considera alias, dígitos verificadores o variantes si la regla está confirmada. Cuando varias filas coincidan, muestra la diferencia de descripción, presentación y origen, y deja la elección visible. Un código corto puede ser válido aunque sea prefijo de otro.
- Previsualiza la importación con recuentos de altas, cambios, filas omitidas y conflictos. Conserva la procedencia para que el operador pueda corregir la hoja. Aplica el lote de forma atómica y comprueba qué hace una segunda importación del mismo archivo. Mantén un identificador estable por registro cuando varios productos puedan compartir un código.

## Diseña para el puesto de trabajo

- Para un lector tipo teclado con sufijo Enter, ofrece un campo enfocado al abrir, búsqueda al recibir el sufijo y devolución del foco al cerrar el resultado. Mientras se edita un producto, respeta el foco del formulario. Conserva una vía manual que use la misma búsqueda.
- Presenta resultados claros para una coincidencia, varias coincidencias y ausencia de resultados. Verifica altas, ediciones y bajas con restricciones persistentes. Si cada equipo tiene su catálogo, entrega respaldo y restauración como mecanismos de traslado acordados.
- Guarda los datos en una ubicación escribible independiente del programa. Un paquete distribuible debe arrancar con un catálogo vacío o ficticio. En Windows, prueba el primer arranque con una cuenta estándar en un equipo limpio, el escaneo físico y la conservación del catálogo al actualizar.

Prueba un código con ceros iniciales, dos longitudes con un prefijo común, un duplicado que cambia la presentación, el mismo registro en dos hojas, una fila inválida y una importación repetida.
