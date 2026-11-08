# Contexto general

Ultima actualizacion: 2026-11-07

## Que estamos construyendo

**AgroShift AI**: una app web que ayuda a un agricultor a comparar tres planes de rotacion de cultivos para tres temporadas, usando el clima historico de NASA POWER, los datos de su suelo y sus prioridades (agua, suelo y aptitud productiva). Caso de demo: Rio Bueno, Region de Los Rios, Chile.

La meta de la demo: una persona sin conocimientos de programacion elige un punto en el mapa, entiende el clima, ajusta prioridades y compara tres rotaciones con razones claras en menos de dos minutos.

## Equipo y areas

| Area | Archivo de contexto | Responsable |
|------|---------------------|-------------|
| Frontend / UX | `frontend.md` | (por definir) |
| Backend / integracion / despliegue | `backend.md` | (por definir) |
| Datos NASA | `datos-nasa.md` | (por definir) |
| Motor agricola (catalogo y reglas) | `motor-agricola.md` | (por definir) |
| Coordinacion, pitch y QA | este archivo | (por definir) |

## Estado del MVP

- [ ] Mapa con seleccion de punto
- [ ] Formulario de suelo, historial y prioridades
- [ ] Consulta real a NASA POWER y graficos
- [ ] Catalogo de 3 a 5 cultivos
- [ ] Motor de reglas con 3 rotaciones
- [ ] Comparador con explicaciones y limites
- [ ] Despliegue (Vercel + Railway)
- [ ] Pitch y video

## Avisos para todos

Cambios que afectan a mas de un area. Lo mas nuevo arriba. Una linea por aviso, con fecha y area.

- 2026-11-07 (general): nueva regla en `AGENTS.md`: antes de trabajar, buscar si hay una skill del proyecto para la tarea (hay una tabla). Si instalan una skill, agreguenla a esa tabla.

- 2026-11-07 (general): nuevas skills `security-and-hardening`, `security-review` y `cloudflare`. Antes de abrir un PR con codigo, pidanle al agente que use `security-review`.

- 2026-11-07 (general): nuevas skills `fastapi`, `pydantic`, `python-testing-patterns`, `deploy-to-vercel`, `tailwind-4-docs` y `accessibility`. Ojo: `deploy-to-vercel` intenta hacer commit y push solo; pidanle que no lo haga.

- 2026-11-07 (general): todas las skills del equipo estan en `.agents/skills/` (con enlaces en `.claude/skills/`). Hagan `git pull` para tenerlas.

- 2026-11-07 (general): el repo ahora es un monorepo. Antes de trabajar, lean `AGENTS.md` y sigan la skill `documentar-trabajo`.
