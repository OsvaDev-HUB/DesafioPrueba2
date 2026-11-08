# Check automatico de la bitacora

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** ci/check-bitacora

## Que hicimos

Agregamos `.github/workflows/bitacora.yml`. Es un GitHub Action que corre en cada PR hacia `main` y falla si el PR no agrega un archivo nuevo en `docs/bitacora/` (la plantilla no cuenta).

## Por que

La regla de documentar estaba solo escrita en `AGENTS.md` y en la skill, asi que dependia de que el agente la siguiera. Con este check, GitHub muestra una X roja en el PR si falta la bitacora, sin importar que agente use cada persona.

## Como probarlo

Este mismo PR lo prueba: trae esta entrada, asi que el check deberia salir verde. Para ver el caso rojo, abrir un PR sin entrada nueva en la bitacora.

## Lo que queda pendiente o no funciona

- El check todavia no es obligatorio. Hay que agregarlo al ruleset "Proteger main" en GitHub (Settings > Rules > Rulesets).
- Los admin pueden saltarse el ruleset con `--admin`, asi que para ellos el check solo avisa.
- Los PR de Dependabot se saltan el check, porque no escriben bitacora.

## Para el que siga

- Cuando exista codigo, agregar en `.github/workflows/` checks para `pytest` (backend) y `npm run build` (frontend).
