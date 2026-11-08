# 002: Motor de reglas en vez de un modelo de IA

- **Fecha:** 2026-11-07
- **Estado:** aceptada (viene de la propuesta, seccion 8)

## Contexto

Necesitamos comparar rotaciones de cultivos y explicar por que una sale mejor que otra. Tenemos dos dias.

## Decision

Usar un motor determinista con reglas simples y puntajes ponderados, no entrenar un modelo.

## Por que

- Cada puntaje se puede explicar paso a paso, y el jurado evalua validez y transparencia.
- No necesitamos datos de entrenamiento que no tenemos.
- Se puede probar con tests simples.

## Que aceptamos a cambio

Los resultados son comparaciones relativas segun supuestos, no predicciones de rendimiento. La IA narrativa queda como extra opcional si sobra tiempo.
