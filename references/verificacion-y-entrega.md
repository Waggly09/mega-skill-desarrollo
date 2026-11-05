# Verificación y entrega de Savia

## Prueba sobre una copia aislada

- Confirma qué proceso y base utiliza la prueba. Prepara datos sintéticos en una base y directorios temporales. Cuando cambies consultas, transacciones o migraciones, prueba en el motor del entorno objetivo además de la prueba rápida que corresponda. Para migraciones, ensaya tanto la instalación nueva como la actualización desde una versión anterior representativa.
- Usa los comandos de la estación cuando estén disponibles. `savia check quick` cubre cambios acotados, `savia check frontend` el frente web y `savia check backend` la API. Para aislar un defecto, ejecuta el archivo o caso pertinente de `services/api/tests/` con pytest, o la prueba web del flujo en `apps/web/tests/`. Cierra con `git diff --check`.
- En Playwright, espera estados observables de la aplicación. Verifica que el usuario puede completar el recorrido con su perfil y que el cambio sigue presente después de recargar. Reproduce también la denegación con un perfil de otro alcance cuando se hayan tocado permisos.

## Promueve y documenta con evidencia

Consulta `docs/operations/environments-and-releases.md` y `docs/operations/deployment.md` para el destino autorizado. Identifica commit, configuración necesaria, cambio de esquema, prueba en el ambiente previo y procedimiento de reversa. Verifica que la reversa sea compatible con los datos que puedan haberse guardado después de promover.

Para presentar Savia, prepara una ficha por capacidad con el problema operativo, puesto, decisión, evidencia y estado en el entorno evaluado. Usa pantallas o resultados con datos sintéticos cuando el material se comparta. Distingue una capacidad comprobada en el clon, una validada en piloto y una habilitada en producción. Una cifra de ahorro, escalabilidad o cobertura necesita método de medición o una hipótesis identificada.

La autorización para publicar esta skill cubre sus instrucciones. Una entrega del código, los datos, las evidencias o la infraestructura de Savia requiere el destino y alcance autorizados para esa entrega.
