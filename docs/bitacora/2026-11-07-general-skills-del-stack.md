# Skills para el stack del proyecto

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** chore/skills-stack

## Que hicimos

Instalamos seis skills nuevas en el proyecto (quedan en `.agents/skills/` con enlaces en `.claude/skills/`, y registradas en `skills-lock.json`):

- `fastapi` (oficial de FastAPI) y `pydantic` (oficial de Pydantic): para el backend.
- `python-testing-patterns`: tests con pytest, sobre todo para el motor de reglas.
- `deploy-to-vercel` (oficial de Vercel): para publicar el frontend.
- `tailwind-4-docs`: Tailwind 4, que es la version que instala Vite.
- `accessibility`: revisar accesibilidad del frontend.

## Por que

Las skills que teniamos no cubrian FastAPI, pytest, Vercel ni Tailwind 4. Elegimos las que tenian mas instalaciones o venian de los autores oficiales. Para Leaflet y Recharts no instalamos nada porque las opciones tenian muy pocos usuarios.

## Como probarlo

Despues de `git pull`, revisar que las seis carpetas esten en `.agents/skills/`. Todas pasaron el analisis de seguridad del instalador (0 alertas).

## Lo que queda pendiente o no funciona

- `deploy-to-vercel` salio con riesgo "medio" en Snyk. Revisamos el archivo: no tiene scripts, pero le dice al agente que haga `git add .`, commit con prefijo `deploy:` y `git push`. Eso no sigue nuestras reglas (main protegida, commits con "Se ..."). Al usarla, hay que pedirle al agente que despliegue sin hacer commit ni push.

## Para el que siga

- Quien haga el despliegue: usar `deploy-to-vercel` para el frontend y `use-railway` para el backend, y anotar las URL en `docs/contexto/backend.md`.
