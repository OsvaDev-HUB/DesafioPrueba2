# Backend

API de AgroShift AI. Consulta el clima en NASA POWER y corre el motor de reglas que compara rotaciones.

**Stack:** Python + FastAPI. Se despliega en Railway.

## Carpetas

- `app/routers/`: endpoints. Ej: `clima.py` (`GET /api/clima`) y `rotaciones.py` (`POST /api/rotaciones`).
- `app/services/`: logica. `nasa_power.py` (pedir y limpiar datos) y `motor_reglas.py` (filtrar y puntuar rotaciones).
- `app/schemas/`: modelos Pydantic de lo que entra y sale de la API.
- `tests/`: pruebas con pytest, sobre todo del motor de reglas.

Archivos que faltan crear: `app/main.py`, `requirements.txt` y `.env.example`.

## Para correrlo (cuando exista)

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```
