# Inicialización y configuración
 
## Inicializa un nuevo repositorio Git:
1. Crea una nueva carpeta llamada repo-principal para tu proyecto
2. Inicializa un repositorio Git en esa carpeta

## Crea y edita archivos:
1. Crea un archivo README.md con una descripción breve del proyecto.
2. Crea un archivo index.html con una estructura básica de HTML.
3. Verifica el estado del repositorio

## Añade y realiza un commit inicial:
1. Añade los archivos creados al área de preparación (staging area)
2. Realiza un commit inicial con un mensaje descriptivo

## Configura un repositorio remoto:
1. Crea un repositorio en el GitHub
2. Conecta el repositorio remoto a tu repositorio local.
3. Sube los cambios locales al repositorio remoto

# Colaboración y ramas
Desde otra carpeta que se llame repo-secundario en tu ordenador:
1. Clona el repositorio
2. Crea una rama llamada branch-A.
3. Cambia a la nueva rama.
4. Realiza cambios en la nueva rama: Modifica index.html añadiendo un párrafo en el body y añade un nuevo archivo style.css.
5. Añade los cambios y realiza un commit.
6. Mira el historial de commits

# Fusiona ramas y resuelve conflictos
1. Cambia a la rama master
2. Vuelve a cambiar el archivo index.html en la misma línea del párrafo y vuelve a añadirlo y hacer un commit.
3. Intenta fusionar branch-A en master.
4. Al fusionar esa rama, te debe crear un conflicto por las modificaciones hechas anteriormente, resuelvelas quedándote con los últimos cambios realizados, luego añade y realiza un commit para completar la fusión.

# Sincronización y colaboración
1. Sube los cambios fusionados en master al repositorio remoto.
3. Desde tu repositorio original repo-principal, actualiza tu repositorio local con los cambios remotos.
4. Coge ids de dos commits y compara los cambios entre dos commits

# Revertir, restaurar, resetear y gitignore
1. Crea un nuevo archivo llamado script.js
2. Añade un nuevo commit y luego reviertelo.
3. Realiza cambios en un archivo existente, como por ejemplo en el style.css, pero no los añadas al área de preparación
4. Restaura el archivo a su estado original.
5. Documenta tanto que se ha cambiado el archivo como la acción de restaurar el cambio
6. Realiza cambios en un archivo y añádelos al área de preparación.
7. Deshaz los cambios en el área de preparación y deja los archivos en su estado modificado
8. Documenta tanto que se ha cambiado el archivo como la acción de restaurar el cambio

# Configurar .gitignore:
1. Crea en directorio de archivos con la extensión .log y .properties y directorio llamado node_modules.
2. Crea un archivo .gitignore y añade reglas para ignorar esos archivos o directorios creados anteriormente.
3. Documenta que estén esos archivos en el directorio con el comando ls y verifica que los archivos especificados sean ignorados por Git y sube los
cambios al repositorio remoto.

# Limpieza y finalización

1. Elimina la rama branch-A localmente una vez que ya no la necesites.
2. Revisa el historial completo de commits y documenta el flujo de trabajo
3. Sube todos los cambios al repositorio remoto.
