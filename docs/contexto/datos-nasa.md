# Contexto: datos NASA

Ultima actualizacion: 2026-11-07

## Que hace esta area

Consultar NASA POWER (API diaria, comunidad `AG`), limpiar los datos (descartar `-999`), y agrupar por mes: temperatura media y lluvia acumulada. Tambien guardar una respuesta valida como respaldo para la demo, por si la API falla durante el pitch.

## Parametros que usamos

- `T2M`, `T2M_MAX`, `T2M_MIN`: temperatura en °C
- `PRECTOTCORR`: lluvia corregida en mm/dia
- `RH2M`: humedad relativa en %
- `ALLSKY_SFC_SW_DWN`: radiacion solar (opcional)

Punto de demo: Rio Bueno, latitud -40.3, longitud -72.8.

## Como esta hoy

- Todavia no hay codigo. El servicio ira en `backend/app/services/nasa_power.py` y el respaldo en `data/respaldo_nasa/`.

## Pendiente

- Primera consulta real y guardar el JSON de respaldo.
