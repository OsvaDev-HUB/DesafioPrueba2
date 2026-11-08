# Instrucciones para agentes

Este repo es **AgroShift AI**, un proyecto de hackathon (NASA Space Apps 2026) en el que trabajan 5 personas, cada una con su propio agente.

## Regla obligatoria

Antes de empezar cualquier tarea y antes de cada commit, sigue la skill **documentar-trabajo**:

- Archivo: `.agents/skills/documentar-trabajo/SKILL.md` (tambien en `.claude/skills/documentar-trabajo/`).
- Resumen: lee `docs/contexto/` y las ultimas entradas de `docs/bitacora/` antes de trabajar. Al terminar, crea una entrada en la bitacora y actualiza el contexto de tu area.

Si no puedes cargar la skill, lee el archivo directamente. No te la saltes aunque la tarea sea chica.

## Regla: busca una skill antes de trabajar

El repo trae skills para casi todo el stack. Antes de escribir codigo, revisa si hay una skill para lo que vas a hacer y usala.

1. Mira la tabla de abajo.
2. Si tu tarea no aparece, revisa las descripciones de todas las skills:
   ```bash
   grep -h "^description:" .agents/skills/*/SKILL.md
   ```
3. Si encuentras una que sirve, cargala (o lee su `SKILL.md`) antes de empezar. Puedes usar mas de una.
4. Si no hay ninguna, trabaja normal. Si crees que falta una, anotalo en tu entrada de la bitacora.

| Si vas a trabajar en... | Usa estas skills |
|-------------------------|------------------|
| API con FastAPI, endpoints, routers | `fastapi`, `senior-backend` |
| Modelos de entrada y salida (schemas) | `pydantic` |
| Tests en Python, motor de reglas | `python-testing-patterns` |
| Componentes React, pantallas, estado | `senior-frontend`, `vercel-react-best-practices` |
| Tipos de TypeScript | `typescript-advanced-types` |
| Estilos con Tailwind | `tailwind-4-docs` |
| Diseño visual, que se vea bien | `impeccable`, `frontend-design` |
| Accesibilidad (teclado, lectores de pantalla, contraste) | `accessibility` |
| Validar entradas, CORS, manejo de datos externos | `security-and-hardening` |
| Revisar seguridad antes de un PR | `security-review` |
| Base de datos y consultas SQL | `sql-optimization` |
| Desplegar el frontend | `deploy-to-vercel` |
| Desplegar el backend | `use-railway` |
| DNS, WAF o Turnstile de Cloudflare | `cloudflare` |
| Decisiones de arquitectura | `senior-architect` |
| Buscar una skill nueva para instalar | `find-skills` |
| Documentar lo que hiciste (siempre) | `documentar-trabajo` |

Las skills no estan por encima de las reglas del equipo. Si una skill dice algo distinto a este archivo (por ejemplo `deploy-to-vercel` intenta hacer commit y push sola), manda este archivo.

Si alguien instala una skill nueva, tiene que agregarla a esta tabla en el mismo PR.

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
