# 📝 04 - Ramas (Branches) en Git

Este script explica cómo **crear, usar y administrar ramas (branches)** en Git.  
Las ramas permiten trabajar en nuevas funcionalidades o documentos sin afectar el código principal, facilitando el trabajo organizado y colaborativo.

---

## 1️⃣ ¿Qué es una rama en Git?

- Una rama es una **línea independiente de desarrollo**.
- Permite trabajar en cambios sin afectar la rama principal (`main` o `develop`).
- Es una práctica fundamental para mantener proyectos ordenados y seguros.

## 2️⃣ Ver ramas existentes

```bash
git branch
```

- Muestra todas las ramas locales.
- La rama actual aparece marcada con *.
- Para ver ramas locales y remotas:

```bash
git branch -a
```

## 3️⃣ Crear una nueva rama

```bash
git branch nombre-rama
```

- Crea la rama, pero no cambia a ella automáticamente.

Ejemplo:
```bash
git branch doc/04-ramas-branches
```

## 4️⃣ Crear y cambiar a una rama en un solo paso

```bash
git checkout -b nombre-rama
```

Ejemplo:
```bash
git checkout -b doc/04-ramas-branches
```

💡 Tip: Es la forma más común de crear ramas para nuevos documentos o funcionalidades.

## 5️⃣ Cambiar entre ramas

```bash
git checkout nombre-rama
```

Ejemplo:
```bash
git checkout develop
```

- Asegúrate de no tener cambios sin commit antes de cambiar de rama.

## 6️⃣ Hacer merge de una rama

- El merge se hace desde la rama destino.

Ejemplo: integrar una rama de documentación a develop:
```bash
git checkout develop
git merge doc/04-ramas-branches
```

- Git intentará combinar automáticamente los cambios.
- Si hay conflictos, deberán resolverse manualmente.

## 7️⃣ Eliminar ramas

Eliminar rama local
```bash
git branch -d nombre-rama
```

Ejemplo:
```bash
git branch -d doc/04-ramas-branches
```
Eliminar rama remota
```bash
git push origin --delete nombre-rama
```

Ejemplo:
```bash
git push origin --delete doc/04-ramas-branches
```

❌ No se puede eliminar la rama en la que estás actualmente.

## 8️⃣ Buenas prácticas al trabajar con ramas

- No trabajar directamente sobre main.
- Usar develop como rama de integración.
Crear ramas por:
- Documento (doc/01-inicializar-repo)
- Funcionalidad (feature/login)
- Corrección (fix/error-commit)
- Eliminar ramas una vez que ya fueron integradas.
- Mantener nombres de ramas claros y descriptivos.

## 9️⃣ Próximo paso
Una vez que sabes trabajar con ramas y merges, el siguiente script
05-pull-push.md explica cómo subir y bajar cambios desde GitHub, usando push y pull.