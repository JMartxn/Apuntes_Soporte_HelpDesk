| Paso | Acción                                | Descripción                                                      | Windows                                  | Linux (ej. Ubuntu)                         |
|------|---------------------------------------|------------------------------------------------------------------|------------------------------------------|--------------------------------------------|
| 1    | **Instalar Git**                      | Git es una herramienta de control de versiones distribuido.      | Descarga el instalador desde: [Git for Windows](https://git-scm.com/download/win) | Usa el gestor de paquetes: `sudo apt install git` |
| 2    | **Verificar instalación**             | Asegúrate de que Git se haya instalado correctamente.            | `git --version`                          | `git --version`                            |
| 3    | **Configurar nombre de usuario**      | Configura tu nombre para identificar tus commits.                | `git config --global user.name "Tu Nombre"` | `git config --global user.name "Tu Nombre"` |
| 4    | **Configurar correo electrónico**     | Configura tu correo para asociarlo con tus commits.              | `git config --global user.email "tu_email@example.com"` | `git config --global user.email "tu_email@example.com"` |
| 5    | **Verificar configuración**           | Verifica que la configuración esté correcta.                     | `git config --global --list`              | `git config --global --list`               |
| 6    | **Crear un repositorio nuevo**        | Inicializa un nuevo repositorio Git en un directorio.            | `git init`                               | `git init`                                 |
| 7    | **Clonar un repositorio**             | Clona un repositorio remoto a tu máquina local.                  | `git clone https://github.com/usuario/repo.git` | `git clone https://github.com/usuario/repo.git` |
| 8    | **Ver el estado de los archivos**     | Muestra los archivos modificados y no versionados.               | `git status`                             | `git status`                               |
| 9    | **Agregar archivos**                  | Añadir archivos para que Git los comitee.                        | `git add archivo`                        | `git add archivo`                          |
| 10   | **Realizar un commit**                | Guarda tus cambios localmente en el repositorio.                 | `git commit -m "Mensaje del commit"`     | `git commit -m "Mensaje del commit"`       |
| 11   | **Subir los cambios (Push)**          | Sube tus commits locales a un repositorio remoto (GitHub, GitLab, etc.). | `git push origin main`                    | `git push origin main`                     |
| 12   | **Obtener cambios (Pull)**            | Trae los cambios del repositorio remoto a tu repositorio local. | `git pull origin main`                    | `git pull origin main`                     |
| 13   | **Ver el historial de commits**       | Muestra los commits realizados.                                  | `git log`                                | `git log`                                  |
| 14   | **Crear una nueva rama**              | Crea una nueva rama para trabajar en una funcionalidad separada. | `git checkout -b nombre-rama`             | `git checkout -b nombre-rama`              |
| 15   | **Cambiar de rama**                   | Cambia entre ramas en el repositorio.                            | `git checkout nombre-rama`               | `git checkout nombre-rama`                 |
| 16   | **Fusionar una rama**                 | Integra los cambios de una rama en la rama actual.               | `git merge nombre-rama`                   | `git merge nombre-rama`                    |
| 17   | **Eliminar una rama**                 | Elimina una rama que ya no se necesita.                          | `git branch -d nombre-rama`               | `git branch -d nombre-rama`                |
| 18   | **Revertir cambios no confirmados**   | Deshace cambios locales no confirmados.                          | `git checkout -- archivo`                | `git checkout -- archivo`                  |
| 19   | **Restaurar a un commit anterior**    | Deshace cambios realizados y regresa a un commit anterior.       | `git reset --hard <hash-del-commit>`      | `git reset --hard <hash-del-commit>`       |
| 20   | **Configurar Git para ignorar archivos** | Define qué archivos o carpetas no deben ser versionados.        | Crear un archivo `.gitignore` en el repositorio y listar archivos o carpetas. | Crear un archivo `.gitignore` en el repositorio y listar archivos o carpetas. |


Explicación de comandos:

    git init: Inicializa un nuevo repositorio Git en el directorio actual.
    git clone <url>: Clona un repositorio remoto a tu máquina local.
    git status: Muestra el estado del repositorio (archivos modificados, sin seguimiento, etc.).
    git add <archivo>: Añade archivos al área de preparación (staging area) para un commit.
    git commit -m "mensaje": Realiza un commit de los archivos que están en el área de preparación.
    git push origin main: Sube los cambios locales al repositorio remoto.
    git pull origin main: Trae los cambios del repositorio remoto a tu repositorio local.
    git log: Muestra el historial de commits.
    git checkout -b <rama>: Crea una nueva rama y cambia a ella.
    git checkout <rama>: Cambia a una rama existente.
    git merge <rama>: Fusiona la rama especificada con la rama actual.
    git branch -d <rama>: Elimina la rama especificada.
    git reset --hard <hash-del-commit>: Restaura el estado del repositorio a un commit anterior.

.gitignore:

Este archivo se usa para decirle a Git qué archivos o directorios no deben ser versionados. Algunos ejemplos de lo que podrías poner en un .gitignore:
# Ignorar archivos temporales de Windows
Thumbs.db
*.bak

# Ignorar carpetas de compilación
/build/
/node_modules/

# Ignorar configuraciones de IDEs
/.idea/
/.vscode/
