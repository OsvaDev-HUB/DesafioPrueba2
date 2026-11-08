# Frontend

App web de AgroShift AI: mapa, formularios, graficos y comparador de rotaciones.

**Stack:** React + TypeScript + Tailwind CSS, Leaflet (mapa) y Recharts (graficos). Se despliega en Vercel.

## Carpetas

- `src/components/`: piezas reutilizables (mapa, ficha de suelo, deslizadores, graficos).
- `src/pages/`: pantallas completas.
- `src/services/`: funciones que llaman a la API del backend.
- `src/types/`: tipos de TypeScript (ej: la forma del JSON de clima).
- `prototipos/`: HTML de pruebas anteriores. No es la app final.

## Para empezar el proyecto

Todavia no esta creado. La idea es usar Vite dentro de esta carpeta:

```bash
npm create vite@latest . -- --template react-ts
npm install
npm run dev
```

El frontend solo habla con el backend, nunca directo con NASA POWER.
