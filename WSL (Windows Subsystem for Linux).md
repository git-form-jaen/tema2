Created: 2024-04-05 17:19
Notetype: #note  
Tags:: #linux #wsl 


**Subsistema de Windows para Linux (WSL)** es una característica de Windows que permite ejecutar un entorno Linux en la máquina Windows, sin necesidad de una máquina virtual independiente ni de arranque dual. WSL está diseñado para proporcionar una experiencia perfecta y productiva para los desarrolladores que quieren usar Windows y Linux al mismo tiempo.

# Actualización de WSL

```cmd
wsl --update
```

# Comprobación de la versión de WSL

```cmd
wsl --version
```

# Enumerar las distribuciones de Linux instaladas

```cmd
wsl -l -v
```

# Ver una lista de las distribuciones de Linux disponibles 

```cmd
wsl --list --online o wsl -l -o
```

# Instalar distribuciones de Linux adicionales

```cmd
wsl --install -d <Distribution Name>
```

# Para ejecutar una distribución de WSL específica sin cambiar la distribución predeterminada

```cmd
wsl -d <DistributionName>
```

# Actualizar paquetes (Ubuntu/Debian)

```bash
sudo apt update && sudo apt upgrade
```

# Construir librerías de Python escritas en C++ en WSL (Debian)

Instala el paquete `python3.11-dev` (`python-dev` contiene los ficheros de cabecera que necesitas para construir extensiones de Python). Además, instala el paquete build-essential

```bash
sudo apt install build-essential
````

# Solucionar bloqueos

Intenta habilitar Hyper-V (si está deshabilitado) e instala WSL desde Microsoft Store. También puede ayudar ejecutar

```
$ sudo apt autoremove -y
```

# Abrir carpeta de WSL en el explorador de Windows

```bash
explorer.exe .
```

# Eliminar ficheros .Identifier al copiar ficheros desde Windows a WSL

https://github.com/microsoft/WSL/issues/4609

```bash
find /path/to/directory -type f -name "*.Identifier" -exec rm -f {} \;
```

