Created: 2023-03-07 16:02
Notetype: #note  
Tags:: #programming #python 

# Introducción

Un entorno de desarrollo o entorno virtual es un mecanismo que nos permite gestionar dependencias. Tienen como objetivo la creación de espacios aislados para cada proyecto. Estos entornos no son compatibles entre distintos sistemas operativos.

---
# Actualizar pip

```cmd
python -m pip install --upgrade pip
```

# Creación de un entorno usando venv (Python 3.6+)

```cmd
python -m venv <Nombre del entorno>
```

Por convención, el entorno se suele nombrar `env`

```cmd
python -m venv env
```

## Activar el entorno de desarrollo

Desde la carpeta del proyecto:

```cmd
env\Scripts\activate
```

```bash
source venv/bin/activate
````

## Desactivar el entorno

```cmd
deactivate
```

### Creación y activación de un entorno de desarrollo en Virtual Studio Code (1.76)

Abre la paleta de comandos (Ctrl+Shift+P) y selecciona el comando `Python: Crear entorno` (Venv o Conda)

#### Solucionar error 'Activate.ps1 cannot be loaded because running scripts is disabled on this system'

Una solución es cambiar la terminal por defecto en VSCode a Command Prompt (CMD) en lugar de PowerShell.

1.  Seleccionar la opción `Seleccionar perfil predeterminado` en el menú desplegable de la terminal.
2.  Seleccionar `Command Prompt`. ![[VS Code - Choosing Default Terminal Profile.png]]

También se puede establecer la política de ejecución como `RemoteSigned` o `Unrestricted` en PowerShell

```cmd
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
``` 
ó
```cmd
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser`
```
(Elimina `-Scope CurrentUser` para que se aplique a todos los usuarios)

---

# Listado e instalación de dependencias (en formato requirements)

```cmd
pip freeze
```

Una buena práctica es almacenar estas dependencias en un archivo llamado `requirements.txt`

```cmd
pip freeze > requirements.txt
```

## Reinstalar las librerías incluidas en el archivo requirements.txt

```cmd
pip install -r requirements.txt
```

# Python Launcher

## Establecer una versión predeterminada específica de Python:

Abre un editor de texto o crea un archivo en `%LOCALAPPDATA%\py.ini`. Agrega el siguiente contenido al archivo `py.ini`:

```
[defaults]
python=3.11
```

Guarda el archivo.

Ahora, cuando ejecutes `py --version` en la consola, debería mostrar la versión predeterminada de Python especificada.
