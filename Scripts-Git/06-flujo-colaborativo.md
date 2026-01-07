# 📝 06 - Flujo colaborativo en Git y GitHub

Este script explica el **flujo de trabajo colaborativo** usando Git y GitHub.  
Incluye el uso de forks, pull requests y la resolución de conflictos, prácticas fundamentales cuando se trabaja en equipo.

---

## 1️⃣ ¿Qué es el flujo colaborativo?

- Es la forma en que **varias personas trabajan sobre un mismo proyecto**.
- Cada colaborador trabaja en su propia rama o fork.
- Los cambios se integran mediante **Pull Requests (Merge Requests)**.
- Permite revisar, aprobar y controlar los cambios antes de unirlos al proyecto principal.

## 2️⃣ Fork de un repositorio

Un **fork** es una copia del repositorio original en tu propia cuenta de GitHub.

### Pasos generales:
1. Ir al repositorio original en GitHub.
2. Hacer clic en el botón **Fork**.
3. GitHub crea una copia en tu cuenta personal.

Luego, clona tu fork:
```bash
git clone git@github.com:usuario/repo.git
```
## 3️⃣ Flujo básico con ramas y Pull Requests

1. Clonar el repositorio o fork
2. Crear una rama nueva
3. Realizar cambios
4. Hacer commit
5. Subir la rama al remoto
6. Crear Pull Request
7. Revisar y hacer merge

Ejemplo:
``` bash
git checkout -b feature/nueva-funcionalidad
git add .
git commit -m "Agrega nueva funcionalidad"
git push -u origin feature/nueva-funcionalidad
```

## 4️⃣ Pull Requests (Merge Requests)

Un Pull Request permite:
- Revisar código antes de integrarlo.
- Discutir cambios con el equipo.
- Mantener la calidad del proyecto.

Buen contenido de un PR:
- Título claro y descriptivo.
- Resumen del cambio.
- Lista de archivos modificados.
- Notas o consideraciones importantes.

## 5️⃣ Resolución de conflictos

- Un conflicto ocurre cuando Git no puede combinar cambios automáticamente.

Pasos para resolver conflictos:
1. Git indicará los archivos con conflicto.
2. Abre el archivo y busca marcas como:

```markdown
<<<<<<< HEAD
Código actual
=======
Código entrante
>>>>>>> rama
```

3. Edita el archivo y conserva el código correcto.
4. Marca el conflicto como resuelto:

```bash
git add archivo-resuelto
git commit
```

💡 Tip: Resolver conflictos con calma y revisar el resultado final.

## 6️⃣ Buenas prácticas en trabajo colaborativo
- No trabajar directamente en main.
- Usar develop como rama de integración.
- Crear ramas por funcionalidad o documento.
- Hacer commits pequeños y claros.
- Revisar PRs antes de hacer merge.
- Eliminar ramas después de integrarlas.
- Comunicar cambios importantes al equipo.

## 7️⃣ Resumen final del flujo Git
```text
main      -> rama estable
develop   -> integración de cambios
feature/* -> nuevas funcionalidades
doc/*     -> documentación
fix/*     -> correcciones
```

Este flujo mantiene el repositorio limpio, ordenado y fácil de mantener.