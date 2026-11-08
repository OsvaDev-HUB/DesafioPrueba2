# Estructura del monorepo y sistema de documentacion

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** refactor/monorepo

## Que hicimos

Ordenamos el repo en carpetas `frontend/`, `backend/`, `data/` y `docs/`, siguiendo la arquitectura de la propuesta (`docs/propuesta/`). Las paginas HTML que ya existian (`FrontEnd.html` y `login.html`) quedaron en `frontend/prototipos/`. Tambien agregamos la skill `documentar-trabajo`, los archivos `AGENTS.md` y `CLAUDE.md`, y las carpetas `docs/contexto/`, `docs/bitacora/` y `docs/decisiones/`.

## Por que

Somos 5 personas trabajando en paralelo, cada una con su agente. Necesitabamos un lugar fijo para cada parte del proyecto y una forma de que todos sepan en que va el resto sin tener que preguntar.

## Como probarlo

No hay codigo que correr todavia. Se puede revisar que la estructura coincida con `docs/arquitectura.md`.

## Lo que queda pendiente o no funciona

- El frontend en React y el backend en FastAPI todavia no estan creados, solo las carpetas.
- `frontend/prototipos/helada-alert.html` es de una idea anterior (alertas de heladas). Puede servir como referencia de la lectura de CSV de NASA POWER, pero no es la app final.

## Para el que siga

- Frontend: crear el proyecto con Vite + React + TypeScript dentro de `frontend/` (ver `frontend/README.md`).
- Backend: crear `backend/requirements.txt` y `backend/app/main.py` con FastAPI (ver `backend/README.md`).
- Repartir las 5 personas en las areas de `docs/contexto/general.md` y escribir los nombres ahi.
