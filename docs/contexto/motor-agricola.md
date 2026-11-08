# Contexto: motor agricola

Ultima actualizacion: 2026-11-07

## Que hace esta area

El catalogo de cultivos y el motor de reglas. El motor es determinista (sin entrenar modelos de IA):

1. Filtra cultivos que no cumplen restricciones fuertes (drenaje, ventana de siembra).
2. Arma secuencias de 3 temporadas evitando repetir la misma familia.
3. Calcula tres subpuntajes de 0 a 100 (agua, suelo, aptitud) y un total ponderado con los pesos de los deslizadores.

Un puntaje de 85/100 solo significa mejor ajuste relativo, no 85 % de rendimiento. Eso tiene que quedar claro en la app.

## Como esta hoy

- Todavia no hay catalogo ni codigo. El catalogo ira en `data/catalogo/` y el motor en `backend/app/services/motor_reglas.py`.

## Pendiente

- Catalogo inicial de 3 a 5 cultivos (por ejemplo trigo, avena, lupino) con fuente de cada dato.
