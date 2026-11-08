# Seguridad de GitHub activada

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** docs/seguridad-github

## Que hicimos

Revisamos y activamos las protecciones de seguridad de GitHub en el repo:

- **Secret scanning y push protection:** ya estaban activas porque el repo es publico. Si alguien intenta subir una clave (Railway, Vercel, una API), GitHub bloquea el push.
- **Dependabot alerts:** las activamos. GitHub avisa si una libreria de `requirements.txt` o `package.json` tiene una vulnerabilidad conocida.
- **Dependabot security updates:** las activamos. Cuando hay una libreria vulnerable, Dependabot abre un PR con la version corregida.

Esto completa lo que quedo pendiente en `2026-11-07-general-skills-seguridad.md`.

## Por que

Con 5 personas y varios agentes trabajando rapido, es facil subir una clave por error o usar una libreria con fallas. Como el repo es publico, una clave subida se ve en minutos.

## Como probarlo

En GitHub: Settings > Code security, las cuatro opciones aparecen activas. Las alertas de Dependabot van a empezar cuando existan `backend/requirements.txt` y `frontend/package.json`.

## Lo que queda pendiente o no funciona

- La cuenta tiene un bloqueo de facturacion, asi que los PR automaticos de Dependabot (que corren sobre Actions) pueden no aparecer hasta que se resuelva. Las alertas si funcionan.
- Los PR de Dependabot no pasan por el check "Bitacora": el workflow los salta a proposito.

## Para el que siga

- Si GitHub bloquea un push por una clave, no la fuercen: saquen la clave del codigo, ponganla en `.env` (que esta en `.gitignore`) y cambien la clave en el servicio, porque ya hay que darla por expuesta.
