# Datos

Datos que usa el backend. El frontend nunca lee esta carpeta directo.

- `catalogo/`: catalogo de cultivos (`cultivos.json`) con familia, meses de siembra y cosecha, temperatura, pH, drenaje y necesidad de agua. Cada dato tiene que decir de donde salio.
- `respaldo_nasa/`: una respuesta real de NASA POWER guardada, para usarla si la API falla en la demo. En la app se tiene que mostrar como "datos de demostracion".
- `postgres/`: opcional. Solo si sobra tiempo para guardar predios. Las migraciones van numeradas: `001_crear_tabla_predios.sql`.
