# DesafioPrueba2

Proyecto del equipo para el hackathon.

## Reglas del repo

La rama `main` esta protegida:

- No se puede hacer push directo a `main`. Todo entra por Pull Request (PR).
- Cada PR necesita 1 aprobacion de otro compañero antes de hacer merge.
- No se puede borrar `main` ni hacer force push.

## Como trabajar

### 1. Clonar el repo (solo la primera vez)

```bash
git clone https://github.com/OsvaDev-HUB/DesafioPrueba2.git
cd DesafioPrueba2
```

### 2. Actualizar main antes de empezar

```bash
git checkout main
git pull
```

### 3. Crear una rama para tu tarea

Una rama por tarea, no por persona.

```bash
git checkout -b feat/nombre-de-la-tarea
```

Nombres de rama segun el tipo de cambio:

- `feat/...` para algo nuevo (ej: `feat/login`)
- `fix/...` para corregir un error (ej: `fix/navbar`)
- `docs/...` para documentacion (ej: `docs/readme`)
- `style/...` para cambios de estilos o formato

### 4. Hacer commits

```bash
git add .
git commit -m "feat: Se agrega el formulario de login"
```

El mensaje va en español, empieza con un prefijo (`feat:`, `fix:`, `docs:`, `style:`, `refactor:`) y despues "Se ...".

### 5. Subir tu rama

```bash
git push -u origin feat/nombre-de-la-tarea
```

### 6. Abrir el Pull Request

En GitHub aparece el boton **Compare & pull request**. Ponle un titulo corto, una descripcion breve y pide revision a un compañero.

### 7. Revisar y hacer merge

- Otro compañero revisa el PR y lo aprueba (no puedes aprobar tu propio PR).
- Con la aprobacion lista, se hace merge a `main`.
- Despues puedes borrar tu rama y volver al paso 2 para la siguiente tarea.

## Si tu rama queda desactualizada

Si alguien hizo merge a `main` mientras trabajabas:

```bash
git checkout main
git pull
git checkout feat/nombre-de-la-tarea
git merge main
```

Si hay conflictos, resuelvelos en los archivos marcados, luego `git add .` y `git commit`.
