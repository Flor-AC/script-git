# 📝 05 - Subir y bajar cambios con Git (Pull & Push)

Este script explica cómo **enviar cambios al repositorio remoto (push)** y cómo  
**obtener cambios desde GitHub (pull)**.  
Estos comandos son esenciales para trabajar de forma colaborativa y mantener el repositorio sincronizado.

---

## 1️⃣ ¿Qué es `git push`?

- `git push` envía los commits locales al repositorio remoto (GitHub).
- Permite que otros colaboradores vean y usen tus cambios.

### Subir cambios al remoto
```bash
git push
```

- Funciona cuando la rama ya está vinculada al remoto.

## 2️⃣ Push de una rama nueva

Cuando creas una rama nueva por primera vez, debes vincularla:

```bash
git push -u origin nombre-rama
```

Ejemplo:
```bash
git push -u origin 05-pull-push
```

- `-u` establece la relación entre la rama local y la remota.
- Después de esto, solo necesitarás usar git push.

## 3️⃣ ¿Qué es git pull?

`git pull` descarga los cambios del repositorio remoto y los integra en tu rama local.

Equivale a:
```bash
git fetch
git merge
```

- Obtener cambios del remoto

```bash
git pull
```

💡 Tip: Haz git pull antes de comenzar a trabajar para evitar conflictos.

## 4️⃣ Ver repositorios remotos

```bash
git remote -v
```

- Muestra los repositorios remotos configurados y sus URLs.
- Normalmente el remoto principal se llama origin.

## 5️⃣ Flujo recomendado de trabajo

```bash 
1. git checkout develop
2. git pull
3. git checkout -b 05-pull-push
4. (realizar cambios)
5. git add .
6. git commit -m "Agrega script 05 - Pull y Push"
7. git push -u origin 05-pull-push
```

- Este flujo ayuda a mantener el repositorio actualizado y ordenado.

## 6️⃣ Errores comunes y recomendaciones

❌ Hacer git push sin haber hecho git pull previamente.
❌ Trabajar directamente sobre main.

✅ Siempre verificar la rama actual con:
```bash
git branch
```

✅ Confirmar cambios antes de subirlos:
```bash
git status
```

## 7️⃣ Próximo paso

El siguiente script 06-flujo-colaborativo.md explica cómo trabajar con:

- Forks
- Pull Requests
- Resolución de conflictos
- Trabajo en equipo con GitHub