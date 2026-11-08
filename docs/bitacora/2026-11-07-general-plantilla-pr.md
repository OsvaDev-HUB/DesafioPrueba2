# Plantilla de PR en vez del check automatico

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** docs/plantilla-pr

## Que hicimos

Desactivamos el workflow "Bitacora" (`.github/workflows/bitacora.yml`) desde GitHub y agregamos `.github/pull_request_template.md`. La plantilla aparece sola al abrir un PR y trae una lista para marcar: entrada en la bitacora, contexto actualizado, aviso si afecta a otros, sin claves y si se probo.

## Por que

La cuenta de GitHub del repo tiene un bloqueo de facturacion que no pudimos resolver, asi que los GitHub Actions no corren. El check salia en rojo en todos los PR aunque trajeran la bitacora, y eso confundia. La plantilla no usa Actions y cumple casi lo mismo: quien revisa ve la lista y confirma.

## Como probarlo

Abrir un PR nuevo en GitHub: la descripcion ya viene con la plantilla.

## Lo que queda pendiente o no funciona

- El archivo del workflow sigue en el repo, solo esta desactivado. Cuando se arregle la facturacion, se vuelve a activar con `gh workflow enable bitacora.yml`.
- La plantilla depende de que la persona sea honesta al marcar y de que quien revisa lo compruebe.
- Los PR automaticos de Dependabot tampoco corren mientras siga el bloqueo (las alertas si llegan).

## Para el que siga

- Al revisar un PR de un compañero, abrir "Files changed" y confirmar que hay un archivo nuevo en `docs/bitacora/` antes de aprobar.
