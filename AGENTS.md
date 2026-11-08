# Instrucciones para agentes

Este repo es **AgroShift AI**, un proyecto de hackathon (NASA Space Apps 2026) en el que trabajan 5 personas, cada una con su propio agente.

## Regla obligatoria

Antes de empezar cualquier tarea y antes de cada commit, sigue la skill **documentar-trabajo**:

- Archivo: `.agents/skills/documentar-trabajo/SKILL.md` (tambien en `.claude/skills/documentar-trabajo/`).
- Resumen: lee `docs/contexto/` y las ultimas entradas de `docs/bitacora/` antes de trabajar. Al terminar, crea una entrada en la bitacora y actualiza el contexto de tu area.

Si no puedes cargar la skill, lee el archivo directamente. No te la saltes aunque la tarea sea chica.

## Mapa del repo

- `frontend/`: app web en React + TypeScript (mapa, formularios, graficos).
- `backend/`: API en Python + FastAPI (clima NASA POWER y motor de reglas).
- `data/`: catalogo de cultivos, respaldo de datos NASA y PostgreSQL opcional.
- `docs/`: propuesta, arquitectura, contexto del equipo, bitacora y decisiones.

La arquitectura completa esta en `docs/arquitectura.md`. La propuesta original esta en `docs/propuesta/`.

## Reglas del equipo

- `main` esta protegida: todo entra por Pull Request con 1 aprobacion.
- Commits en español con prefijo: `feat: Se agrega ...`, `fix: Se corrige ...`.
- No mencionar IA, Claude ni asistentes en commits, PR, codigo ni documentacion.
- Codigo sencillo, nombres claros y comentarios cortos en español.
