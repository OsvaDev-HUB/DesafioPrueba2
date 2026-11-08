# Regla para buscar skills antes de trabajar

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** docs/regla-buscar-skills

## Que hicimos

Agregamos a `AGENTS.md` una regla nueva: antes de escribir codigo, el agente tiene que revisar si hay una skill del proyecto para esa tarea. Pusimos una tabla que dice que skill usar segun el tipo de trabajo (FastAPI, React, Tailwind, tests, seguridad, despliegue, etc.) y un comando para leer las descripciones de todas.

## Por que

Ya tenemos 20 skills en el repo, pero no sirven si el agente no sabe que existen. La tabla hace que encontrar la correcta sea rapido, y como `AGENTS.md` se carga siempre, todos los agentes la ven.

## Como probarlo

Pedirle a un agente una tarea de FastAPI y revisar que cargue `fastapi` antes de escribir codigo.

## Lo que queda pendiente o no funciona

- Igual que la regla de documentar, es una instruccion: el agente casi siempre la sigue, pero nada lo obliga.
- La tabla hay que mantenerla a mano cuando se agreguen skills.

## Para el que siga

- Si instalan una skill nueva, agregarla a la tabla de `AGENTS.md` en el mismo PR.
