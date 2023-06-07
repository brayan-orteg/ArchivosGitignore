# ArchivosGitignore
Tarea para enterder el uso de los archivos .gitgnore

El archivo .gitignore es un archivo de texto que le dice a Git qué otros archivos y carpetas de un proyecto debe ignorar.

Un archivo .gitignore local se coloca normalmente en el directorio de origen de un proyecto. También puedes crear un archivo .gitignore global y cualquier entrada que contenga será ignorada en todos tus repositorios Git por igual.

Para crear un archivo .gitignore local, crea un archivo de texto y llámalo .gitignore (recuerda incluir el . al principio). Después edita el archivo como sea necesario. Cada línea nueva debería contener el archivo o carpeta que quieres que Git ignore.

Las entradas en este archivo también pueden seguir un modelo similar.

    * se usa para encontrar coincidencias
    / se usa para ignorar nombres de ruta relacionados con el archivo .gitignore
    # se usa para añadir comentarios al archivo .gitignore

Este es un ejemplo de cómo se vería un archivo .gitignore:
# Ignorar todos los archivos de texto
*.txt

# Ignorar archivos relacionados con claves de una API
.env

# Ignorar archivos de configuración SASS
.sass-cache

Para añadir o cambiar tu archivo .gitignore global, ejecuta el siguiente comando:
git config --global core.excludesfile ~/.gitignore_global
Esto creará el archivo  ~/.gitignore_global. Ahora puedes editar ese archivo de la misma manera que un archivo .gitignore local. Todos tus repositorios Git ignorarán los archivos y carpetas que aparecen enumerados en el archivo .gitignore global.

Para dejar de seguir un único archivo, es decir, dejar de rastrear el archivo, pero no eliminarlo del sistema puedes usar:
git rm --cached filename
Primero confirma cualquier cambio pendiente en el código y después ejecuta:
git rm -r --cached
Esto elimina cualquier archivo modificado del área de staging, después ejecuta:
git add .
Confírmalo:
git commit -m ".gitignore is now working"
Para deshacer git rm --cached filename, use git add filename

