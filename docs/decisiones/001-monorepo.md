# 001: Usar un monorepo

- **Fecha:** 2026-11-07
- **Estado:** aceptada

## Contexto

Somos 5 personas en un hackathon de dos dias, con un solo producto que tiene frontend, backend y datos.

## Decision

Un solo repo con carpetas `frontend/`, `backend/`, `data/` y `docs/`. Nada de varios repos ni microservicios.

## Por que

- Un solo `git clone` y un solo lugar para los PR.
- Un cambio que toca frontend y backend se revisa en el mismo PR.
- La documentacion del equipo (`docs/contexto/` y `docs/bitacora/`) queda junto al codigo.

## Que aceptamos a cambio

Si el proyecto creciera mucho, habria que separar partes. Para el hackathon no hace falta.
