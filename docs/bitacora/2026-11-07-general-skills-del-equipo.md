# Skills compartidas para todo el equipo

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** chore/skills-equipo

## Que hicimos

Subimos al repo las skills que estaban solo en un computador: `find-skills`, `frontend-design`, `impeccable`, `senior-architect`, `senior-backend`, `senior-frontend`, `sql-optimization`, `typescript-advanced-types`, `use-railway` y `vercel-react-best-practices`. Los archivos reales estan en `.agents/skills/` y en `.claude/skills/` hay enlaces a ellos. Tambien subimos `skills-lock.json`, que guarda de donde salio cada skill.

## Por que

Asi las 5 personas tienen las mismas skills al hacer `git pull`, sin instalarlas una por una.

## Como probarlo

Despues de `git pull`, revisar que existan `.agents/skills/` y `.claude/skills/` con las mismas carpetas.

## Lo que queda pendiente o no funciona

- En Windows los enlaces de `.claude/skills/` pueden aparecer como archivos de texto. Si pasa, hay que abrir la skill directo desde `.agents/skills/`.

## Para el que siga

- Si alguien instala una skill nueva, tiene que subirla en un PR y avisar en `docs/contexto/general.md`.
