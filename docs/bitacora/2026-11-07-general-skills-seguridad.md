# Skills de seguridad y Cloudflare

- **Fecha:** 2026-11-07
- **Area:** general
- **Persona:** Osvaldo Uhart
- **Rama / PR:** chore/skills-seguridad

## Que hicimos

Instalamos tres skills nuevas en `.agents/skills/` (con enlaces en `.claude/skills/`):

- `security-and-hardening` (Addy Osmani): para escribir codigo seguro desde el principio, como validar entradas, configurar CORS y no mostrar errores internos.
- `security-review` (Sentry): para revisar el codigo buscando vulnerabilidades antes de abrir un PR.
- `cloudflare` (oficial de Cloudflare): para elegir productos de Cloudflare, por ejemplo WAF, Turnstile o DNS.

## Por que

La app no tiene login, asi que los riesgos principales son subir claves al repo, dejar CORS abierto, no validar lo que llega a la API (latitud, longitud, pH) y usar dependencias con vulnerabilidades. Las dos primeras skills cubren eso. La de Cloudflare la pidio el equipo por si ponemos Cloudflare delante de la app.

## Como probarlo

Todas pasaron el analisis del instalador. `security-review` marco 1 alerta: la revisamos y es solo documentacion en Markdown, sin scripts. La alerta viene de los ejemplos de codigo vulnerable que muestra a proposito.

## Lo que queda pendiente o no funciona

- Hoy desplegamos en Vercel y Railway, no en Cloudflare. La skill de Cloudflare solo sirve si decidimos usar su DNS, WAF o Turnstile. Si alguien quiere mover el despliegue a Cloudflare, tiene que ser una decision escrita en `docs/decisiones/`.
- Falta activar en GitHub el secret scanning y las alertas de Dependabot.

## Para el que siga

- Antes de abrir un PR con codigo del backend, pedirle al agente que use `security-review`.
