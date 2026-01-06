# 📝 Guía Completa de Scripts Git

Bienvenido a esta guía práctica de Git, diseñada tanto para uso personal como para enseñanza.  
Aquí encontrarás desde la inicialización de un repositorio hasta flujos colaborativos, resolución de conflictos y buenas prácticas, con ejemplos claros y fáciles de seguir.

---

## 01 - Inicializar un repositorio Git

### Crear un repositorio local
```bash
git init
Crea un repositorio Git en la carpeta actual.

✅ Tip: Verifica que se haya creado .git/ con ls -a.

Configurar usuario y correo
bash
git config --global user.name "Nombre del usuario"
git config --global user.email "nombreusuario@correo.com"
Esto asigna tu nombre y correo a todos los commits.

Nota: Omite --global si solo quieres configurar un repositorio específico.

Revisar configuración
bash
git config --list
Muestra todas las configuraciones activas de Git.

Crear archivo README
bash
echo "# Script Git" >> README.md
git add README.md
git commit -m "Agrega README inicial"
Siempre es buena práctica iniciar con un README.

Conectar con repositorio remoto
bash
git remote add origin git@github-personal:Flor-AC/script-git.git
git push -u origin main
-u vincula la rama local con la remota para futuros push/pull.