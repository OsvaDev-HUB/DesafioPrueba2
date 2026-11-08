---
name: documentar-trabajo
description: OBLIGATORIA en este repo. Usar SIEMPRE al empezar cualquier tarea (para leer el contexto del equipo) y SIEMPRE al terminarla o antes de hacer commit o PR (para dejar escrito lo que se hizo). Aplica a cualquier cambio de codigo, datos, configuracion o documentacion en AgroShift AI, aunque sea chico. Tambien usar cuando alguien pregunte "en que va el proyecto", "que hizo el resto", "que falta" o "donde quedo esto".
---

# Documentar el trabajo

En este proyecto trabajamos 5 personas, cada una con su propio agente. Los agentes no comparten memoria entre si: lo unico que todos ven es el repo. Por eso cada agente tiene que **leer el contexto antes de trabajar** y **dejar escrito lo que hizo al terminar**, en palabras que entienda tanto una persona del equipo como el proximo agente.

Si no se documenta, el trabajo se pierde para los demas, aunque el codigo este en `main`.

## Donde se escribe

```
docs/
├── contexto/      # como esta cada area HOY (se reescribe, no se acumula)
│   ├── general.md
│   ├── frontend.md
│   ├── backend.md
│   ├── datos-nasa.md
│   └── motor-agricola.md
├── bitacora/      # una entrada por tarea terminada (se acumula, no se edita)
│   └── _plantilla.md
└── decisiones/    # decisiones importantes y su porque
```

- **contexto/** responde "como esta esto ahora". Se actualiza: se borra lo viejo y se deja lo actual.
- **bitacora/** responde "que se hizo y por que". Cada tarea crea su propio archivo nuevo, asi 5 personas no se pisan en el mismo archivo.
- **decisiones/** es para cosas que cambian como trabaja el resto (elegir una libreria, cambiar el formato de la API, quitar una funcion del MVP).

## Paso 1: antes de empezar (leer)

1. Lee `AGENTS.md` en la raiz.
2. Lee `docs/contexto/general.md` completo, sobre todo la seccion **Avisos para todos**.
3. Lee el archivo de contexto de tu area (`docs/contexto/<area>.md`). Si la tarea toca otra area, lee tambien ese.
4. Lee las ultimas 5 entradas de `docs/bitacora/` (los nombres empiezan con la fecha, asi que las ultimas son las de nombre mayor):
   ```bash
   ls docs/bitacora | grep -v '^_' | sort | tail -5
   ```
5. Si algo de lo que leiste contradice lo que te pidieron, avisale a la persona antes de seguir.

## Paso 2: mientras trabajas

- Si tomas una decision que afecta a otra area (nombre de un endpoint, forma de un JSON, una libreria nueva), anotala en ese momento para no olvidarla.
- Si descubres algo que no funciona y no lo vas a arreglar, anotalo tambien.

## Paso 3: al terminar (escribir)

Haz esto antes del commit, para que la documentacion vaya en el mismo PR que el codigo.

1. **Crea una entrada en la bitacora** copiando `docs/bitacora/_plantilla.md` a:
   ```
   docs/bitacora/AAAA-MM-DD-<area>-<tarea-corta>.md
   ```
   Ejemplo: `docs/bitacora/2026-11-08-backend-endpoint-clima.md`. Usa la fecha real de hoy.

2. **Actualiza el contexto de tu area** (`docs/contexto/<area>.md`): que funciona, que esta a medias, que falta. Borra lo que ya no es cierto. Este archivo tiene que leerse en menos de 2 minutos.

3. **Si tu cambio afecta a otra area**, agrega una linea en la seccion **Avisos para todos** de `docs/contexto/general.md`, con fecha. Ejemplo:
   > - 2026-11-08 (backend): `GET /api/clima` ahora devuelve la temperatura en `temp_media_c`, no en `t2m`. El frontend tiene que cambiar el nombre.

4. **Si fue una decision importante**, crea `docs/decisiones/NNN-titulo.md` con el siguiente numero libre (contexto, decision, por que, que aceptamos a cambio).

Solo edita el contexto de tu area y la seccion de avisos. No reescribas el contexto de otra area: si ves algo mal ahi, ponlo como aviso.

## Como escribir (redaccion humana)

Escribe como lo haria un compañero del equipo que le explica a otro lo que hizo. Estas reglas son obligatorias:

- **Español simple y frases cortas.** Nada de jerga innecesaria.
- **Primera persona del plural:** "agregamos", "dejamos", "falta". Nunca "el agente hizo" ni "como modelo de IA".
- **No menciones a la IA**, ni a Claude, ni a ningun asistente o herramienta de IA. El trabajo es del equipo.
- **Explica el porque**, no solo el que. "Usamos caché porque la API de NASA a veces tarda 10 segundos" sirve mas que "se agrega caché".
- **Se honesto.** Si algo no se probo, escribe "no lo probamos". Si algo falla a veces, dilo. No inventes resultados ni numeros.
- **Fechas reales** (2026-11-08), nunca "hoy" o "ayer".
- **Rutas exactas** de archivos (`backend/app/services/nasa_power.py`) para que se puedan abrir directo.
- **Sin bloques de codigo largos.** Si hace falta, maximo 10 lineas; para lo demas, apunta al archivo.
- **Sin emojis.**

Ejemplo malo:
> Se implemento exitosamente una robusta capa de servicios para optimizar la integracion con la API.

Ejemplo bueno:
> Agregamos `backend/app/services/nasa_power.py`, que pide temperatura y lluvia a NASA POWER y las agrupa por mes. Lo probamos con Rio Bueno (-40.3, -72.8) para 2025 y funciona. Todavia no maneja cuando la API se cae: eso queda pendiente.

## Escribir para el proximo agente

Cada entrada de bitacora termina con la seccion **Para el que siga**. Es lo que el proximo agente (o persona) necesita para continuar sin preguntar:

- Que es lo siguiente que hay que hacer, en concreto.
- Que archivos tocar.
- Como probarlo (comando exacto si existe).
- Preguntas abiertas o cosas que hay que confirmar con alguien del equipo.

## Lista rapida antes del commit

- [ ] Lei el contexto antes de empezar.
- [ ] Cree mi entrada en `docs/bitacora/` con fecha real.
- [ ] Actualice `docs/contexto/<mi-area>.md`.
- [ ] Si afecta a otros, deje un aviso en `docs/contexto/general.md`.
- [ ] Todo esta escrito en español simple, sin mencionar IA y sin emojis.
