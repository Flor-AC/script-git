# 📝 02 - Agregar archivos al staging en Git

Este script muestra cómo **agregar archivos al área de staging** en Git, prepararlos para commit y revisar su estado. Es una guía práctica y didáctica, ideal para uso personal y para enseñar a alumnos.

---

## 1️⃣ Agregar un archivo específico

```bash
git add nombre-archivo
```
- Prepara un solo archivo para el próximo commit.
✅ Tip: Útil cuando estás trabajando en varios archivos y quieres commitear solo uno.
Ejemplo:
```bash
git add README.md
```

## 2️⃣ Agregar todos los archivos modificados

```bash
git add .
```
- Agrega todos los cambios nuevos o modificados en la carpeta actual y subcarpetas.
✅ Tip: Muy práctico cuando terminas un conjunto de cambios relacionados.

Ejemplo:
```bash
git add .
git status
git status mostrará qué archivos están listos para commit.
```

## 3️⃣ Revisar el estado del repositorio

```bash
git status
```
Muestra:
- Archivos staged (listos para commit)
- Archivos modificados pero no staged
- Archivos no rastreados

💡 Tip: Revisa siempre el estado antes de hacer commit para evitar olvidar archivos importantes.

## 4️⃣ Tips y buenas prácticas

- Hacer commits pequeños y frecuentes facilita el seguimiento de cambios.
- Siempre revisa git status antes de git commit.
- No agregues archivos innecesarios al staging, como binarios o temporales, usa .gitignore.

Ejemplo de uso de .gitignore:
```bash
# Ignorar archivos temporales
*.log
*.tmp
node_modules/
```
- Después de hacer git add, el siguiente paso natural es hacer commit de los cambios.

## 5️⃣ Próximo paso
Una vez que tus archivos están en staging, el siguiente script 03-commits.md muestra cómo guardar esos cambios con un commit, incluyendo mensajes descriptivos y revisión de historial.