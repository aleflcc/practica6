# Cuenten el viaje — Bitácora de la Práctica 6

## 1. El flujo de Git Flow y la utilidad de las ramas
En este taller implementamos el flujo de trabajo **Git Flow** para coordinar los avances de la misión espacial sin interferir entre equipos:
- **`main`**: Funcionó como el entorno de producción estable. Solo contiene versiones finales, probadas y consolidadas del proyecto.
- **`develop`**: Fue la rama principal de integración continua. Aquí fuimos uniendo los avances de las distintas fases antes de liberarlas a producción.
- **`feature/*`** (`feature/aurora-lanzamiento`, `feature/orbita-aterrizaje`, `feature/conflicto-orbita`): Sirvieron como ramas de trabajo aislado. Cada equipo desarrolló sus tareas específicas en ellas sin arriesgar la estabilidad de `develop` ni `main`.

---

## 2. Creación de ramas, commits y Pull Requests
- **Creación y trabajo local:** Cada equipo creó su rama de característica a partir de `develop` para trabajar en sus archivos correspondientes (`misiones/aurora.md` y `misiones/orbita.md`).
- **Commits y subida:** Tras redactar los cambios en VS Code, confirmamos los avances localmente con commits descriptivos y los subimos a GitHub.
- **Pull Requests (PR):** Abrimos las solicitudes de extracción desde nuestras ramas `feature/*` dirigidas hacia `develop`. En la descripción del PR detallamos el problema resuelto, los archivos modificados, la forma de comprobación y la lista de verificación.

---

## 3. Revisión cruzada, conflicto y publicación en `main`
- **Revisión del otro equipo:** El equipo receptor revisó en la pestaña *Files changed* que no hubiera cambios indeseados en archivos fuera de la misión asignada y validó el cumplimiento del checklist antes de aprobar la fusión.
- **Resolución del conflicto:** Para simular la concurrencia, modificamos la misma línea en `panel/estado.md` con estados distintos para Aurora y Órbita. Al intentar fusionar `develop` en la rama de trabajo, Git detectó el choque (`CONFLICT`). Abrimos el archivo en VS Code, eliminamos manualmente los marcadores (`<<<<<<<`, `=======`, `>>>>>>>`), consensuamos el mensaje unificado del estado de la misión y completamos el commit de resolución.
- **Publicación final:** Una vez resuelto e integrado todo en `develop`, abrimos un PR final desde `develop` hacia `main` para publicar la versión oficial y libre de errores en producción.

---

## 4. Comandos clave utilizados y su utilidad

1. `git checkout -b <nombre-rama>`
   - **Por qué fue útil:** Nos permitió crear una nueva rama de trabajo e ingresar a ella en un solo paso, asegurando que los cambios no se hicieran directamente en `develop` o `main`.

2. `git merge develop`
   - **Por qué fue útil:** Sirvió para traer las actualizaciones de la rama de integración a nuestra rama de característica. Fue el comando clave que desencadenó y nos permitió detectar el conflicto en `panel/estado.md` para resolverlo localmente antes de subir los cambios.

3. `git pull origin main` (o `develop`)
   - **Por me fue útil:** Nos permitió sincronizar nuestro repositorio local en la terminal descargando las últimas fusiones y commits realizados por el equipo en GitHub, manteniendo el entorno actualizado.
