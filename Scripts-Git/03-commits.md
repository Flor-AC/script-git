# 📝 03 - Trabajar con commits en Git

Este script muestra cómo **guardar los cambios en tu repositorio usando commits**, cómo ver el historial y cómo modificar commits recientes.  
Es ideal para uso personal y para enseñanza a alumnos, con ejemplos claros y prácticos.

---

## 1️⃣ Crear un commit

```bash
git commit -m "Mensaje descriptivo"
```
- Un commit guarda los cambios preparados en el staging area.

💡 Tip: Usa mensajes claros y concisos que describan qué se hizo y por qué.

Ejemplo:
```bash
git add README.md
git commit -m "Agrega sección de configuración inicial"
```

## 2️⃣ Ver historial de commits

```bash
git log
```

- Muestra todos los commits de la rama actual, con información de autor, fecha y mensaje.

💡 Tip: Para un resumen compacto, usa:

```bash
git log --oneline
```

Ejemplo de salida:
```powershell
a1b2c3d Agrega sección de configuración inicial
e4f5g6h Inicializa repositorio con README
```

## 3️⃣ Modificar el último commit

```bash
git commit --amend -m "Nuevo mensaje de commit"
```

- Útil si olvidaste agregar archivos o quieres mejorar el mensaje del commit anterior.

❌ Precaución: No usar --amend si el commit ya fue enviado al remoto y otros colaboradores están trabajando sobre él.

Ejemplo:
```bash
git add . 
git commit --amend -m "Agrega README y sección de configuración inicial"
```

## 4️⃣ Deshacer un commit local

- Para deshacer el último commit pero mantener los cambios en staging:
```bash
git reset --soft HEAD~1
```
- Para deshacer el último commit y descartar los cambios:
```bash
git reset --hard HEAD~1
```

💡 Tip: Siempre verifica con git log y git status antes de usar reset.

## 5️⃣ Buenas prácticas con commits

- Hacer commits pequeños y frecuentes ayuda a mantener un historial limpio.
- Siempre escribe mensajes descriptivos y claros.
- Evita hacer commits enormes que mezclen muchas funciones distintas.
- Revisa siempre el estado del repo (git status) antes de commitear.

## 6️⃣ Próximo paso

Una vez que tus commits están listos, el siguiente script 04-ramas-branches.md muestra cómo trabajar con ramas, crear nuevas, hacer merges y mantener tu repositorio organizado.