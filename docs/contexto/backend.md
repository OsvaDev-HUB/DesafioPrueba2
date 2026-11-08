# Contexto: backend

Ultima actualizacion: 2026-11-07

## Que hace esta area

API propia en Python + FastAPI. Recibe la ubicacion, el suelo y las prioridades desde el frontend, pide el clima a NASA POWER (con cache), llama al motor de reglas y devuelve JSON. Tambien se encarga del despliegue (Railway para la API, Vercel para el frontend).

## Como esta hoy

- Todavia no hay codigo. Solo las carpetas en `backend/app/` y `backend/tests/`.

## Endpoints planeados

Esto es una propuesta; cuando se cambie, avisar en `general.md`.

- `GET /api/clima?lat=..&lon=..&inicio=AAAAMMDD&fin=AAAAMMDD`: clima mensual de la ubicacion.
- `POST /api/rotaciones`: recibe suelo y prioridades, devuelve 3 planes con puntajes y explicaciones.

## Pendiente

- `requirements.txt`, `app/main.py` y el primer endpoint.
