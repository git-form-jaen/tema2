Created: 2024-11-30 16:41
Notetype: #note  
Tags:: #programming #ide 

# Basic Editing

## Multiple selections (multi-cursor)

VS Code supports multiple cursors for fast simultaneous edits. You can add secondary cursors (rendered thinner) with Alt+Click. Each cursor operates independently based on the context it sits in. A common way to add more cursors is with Ctrl+Alt+Down or Ctrl+Alt+Up that insert cursors below or above.

> [!note]
> Your graphics card driver (for example NVIDIA) might overwrite these default shortcuts.

![[Visual Studio Code - multicursor.gif]]

Ctrl+D selects the word at the cursor, or the next occurrence of the current selection.

![[Visual Studio Code - multicursor-word.gif]]

> **Tip:** You can also add more cursors with Ctrl+Shift+L, which will add a selection at each occurrence of the current selected text


# Extensiones recomendadas

## Visual Studio Code

- IntelliCode ([Microsoft](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode))
- Live Share ([Microsoft](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare))
- GitHub Copilot ([GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot))
- Spanish Language Pack for Visual Studio Code ([Microsoft](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-es))
- Visual Studio Code Remote Development Extension Pack ([Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack))
- vscode-icons ([VSCode Icons Team](https://marketplace.visualstudio.com/publishers/vscode-icons-team))
- Peacock ([John Papa](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock))
- Better Comments ([Aaron Bond](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments))
- CodeSnap ([adpyke](https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap))
- CodeTour ([Jonathan Carter](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour))
- Code Runner ([Jun Han](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner))
- Path Intellisense ([Christian Kohler](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense))
## Markdown

 - Markdown Preview Mermaid Support ([Matt Bierner](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid))
## Python

- Python ([Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-python.python))
- Ruff ([Astral Software](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff))
- Even Better TOML ([tamasfe](https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml))
- autoDocstring ([Nils Werner](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring))
- Python Environment Manager ([Don Jayamanne](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-environment-manager))
## Python Data

- Jupyter ([Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter))
- Data Wrangler ([Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.datawrangler))
- Rainbow CSV ([mechatroner](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv))
## Git/GitHub

- Git Blame ([Wade Anderson](https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame))
- Git Graph ([mhutchie](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph))
- Git History ([Don Jayamanne](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory))
- GitHub Pull Requests ([GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github))
- GitHub Repositories ([Github](https://marketplace.visualstudio.com/items?itemName=GitHub.remotehub))
- GitHub Actions ([GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions))

# Keyboard shortcuts

## General

**Atajos de teclado**: Ctrl+K Ctrl+S
**Paleta de comandos**:  Ctrl+Shift+P
**Terminal**: Ctrl+Shift+Ñ
**Quick Open**: Ctrl+P
**Quick Open (multiple files)**: Right Arrow (→) to open the selected file but leave dropdown available
**Navigate Tabs**: Ctrl+Tab
**Abrir configuración**: Ctrl+,
**Cerrar carpeta**: Ctrl+K F
**Nuevo archivo**: Ctrl+N
**Cambiar lenguaje del archivo**: Ctrl+K M
**Mostrar en el explorador de ficheros**: Shift+Alt+R
## Display

**Toggle Sidebar**: Ctrl+B
**Show Explorer view**: Ctrl+Shift+E

## Editor

**Multi Cursor**: Alt+Click
**Multi Cursor (above / below)**: Ctrl+Alt+Up / Ctrl+Alt+Down
**Copy line up / down**: Shift+Alt+Up / Shift+Alt+Down
**Move line up and down**: Alt+Up / Alt+Down

**Select Line**: Ctrl+L
**Select all occurrences of current word**: Ctrl+F2
**Select next occurrence of current word**: Ctrl+D
**Rename Symbol**: F2

**Navigate to beginning and end of file**: Ctrl+Home / Ctrl+End
**Code folding**: Ctrl+K Ctrl+L
**Plegar todo**: Ctrl+K Ctrl+0
**Desplegar todo**: Ctrl+K Ctrl+J
**Go to definition**: F12
**Peek definition**: Alt+F12

**Toggle block comment**: Shift+Alt+A
**Buscar y reemplazar**: Ctrl+H
**Go to line**: Ctrl+G
**Side by side editing**: Ctrl+\
**Switch between editors**: Ctrl+1, Ctrl+2
**Close editor**: Ctrl+F4

**Refactoring**: Ctrl+.
## File management

**Save as**: Ctrl+Shift+S
**Show active file in new window/instance**: Ctrl+K O

## Python

**IntelliSense**: Ctrl+Space
**Ejecutar línea de código Python**: Shift+Enter
**Debugger**: F5

## C/C++

**Iniciar compilación**: Ctrl+Shift+B
[[Visual Studio Code - keyboard-shortcuts-windows.pdf|(PDF) Referencia - Keyboard Shortcuts]]

# Settings

## User Settings

Depending on your platform, the user settings file is located here:

    Windows %APPDATA%\Code\User\settings.json
    macOS $HOME/Library/Application\ Support/Code/User/settings.json
    Linux $HOME/.config/Code/User/settings.json

### Format on paste

```
"editor.formatOnPaste": true
```

### Interactive Jupyter

- **Interactive Python**: Search for `Jupyter Interactive Window` → Enable (When pressing shift + enter, send selection to Jupyter interactive window as opposed to the Python terminal)
![[Visual Studio Code - Settings for Jupyter.png]]


- **Root**: Regarding changing the root folder for Jupyter notebooks, you can modify your settings in VS Code by including the JSON snippet below: 

```json
"settings": {
		"jupyter.notebookFileRoot": "${workspaceFolder}/app",
	}
```


## Workspace Settings (.vscode/settings.json)

```json
{
    // Python settings
    "python.analysis.autoSearchPaths": true,
    "python.analysis.diagnosticSeverityOverrides": {
        "reportMissingImports": "none"
    },
    "python.envFile": "${workspaceFolder}/.env",
    "python.terminal.activateEnvironment": true,
    "python.defaultInterpreterPath":"${workspaceFolder}/.venv/bin/python",

    // Test settings
    "python.testing.pytestEnabled": true,
    "python.testing.unittestEnabled": false,
    "python.testing.cwd": "${workspaceFolder}/tests",
    "python.testing.pytestPath": "${workspaceFolder}/.venv/bin/pytest",
    "python.testing.autoTestDiscoverOnSaveEnabled": true
}
```

# Comandos

## Open code with current directory
`code .`
## Open diff editor
`code --diff <file1> <file2>`

# [[Emmet VSCode|Emmet]]

# IntelliSense

VS Code IntelliSense offers different types of completions, including language server suggestions, snippets, and simple word based textual completions.

![[Visual Studio Code - IntelliSense Icons.png]]

# Variables

## [Predefined variables](https://code.visualstudio.com/docs/editor/variables-reference#_predefined-variables)

The following predefined variables are supported:

- **${userHome}** - the path of the user's home folder
- **${workspaceFolder}** - the path of the folder opened in VS Code
- **${workspaceFolderBasename}** - the name of the folder opened in VS Code without any slashes (/)
- **${file}** - the current opened file
- **${fileWorkspaceFolder}** - the current opened file's workspace folder
- **${relativeFile}** - the current opened file relative to `workspaceFolder`
- **${relativeFileDirname}** - the current opened file's dirname relative to `workspaceFolder`
- **${fileBasename}** - the current opened file's basename
- **${fileBasenameNoExtension}** - the current opened file's basename with no file extension
- **${fileExtname}** - the current opened file's extension
- **${fileDirname}** - the current opened file's folder path
- **${fileDirnameBasename}** - the current opened file's folder name
- **${cwd}** - the task runner's current working directory upon the startup of VS Code
- **${lineNumber}** - the current selected line number in the active file
- **${selectedText}** - the current selected text in the active file
- **${execPath}** - the path to the running VS Code executable
- **${defaultBuildTask}** - the name of the default build task
- **${pathSeparator}** - the character used by the operating system to separate components in file paths
### [Predefined variables examples](https://code.visualstudio.com/docs/editor/variables-reference#_predefined-variables-examples)

Supposing that you have the following requirements:

1. A file located at `/home/your-username/your-project/folder/file.ext` opened in your editor;
2. The directory `/home/your-username/your-project` opened as your root workspace.

So you will have the following values for each variable:

- **${userHome}** - `/home/your-username`
- **${workspaceFolder}** - `/home/your-username/your-project`
- **${workspaceFolderBasename}** - `your-project`
- **${file}** - `/home/your-username/your-project/folder/file.ext`
- **${fileWorkspaceFolder}** - `/home/your-username/your-project`
- **${relativeFile}** - `folder/file.ext`
- **${relativeFileDirname}** - `folder`
- **${fileBasename}** - `file.ext`
- **${fileBasenameNoExtension}** - `file`
- **${fileDirname}** - `/home/your-username/your-project/folder`
- **${fileExtname}** - `.ext`
- **${lineNumber}** - line number of the cursor
- **${selectedText}** - text selected in your code editor
- **${execPath}** - location of Code.exe
- **${pathSeparator}** - `/` on macOS or linux, `\` on Windows

> [!tip]
> **Tip**: Use IntelliSense inside string values for `tasks.json` and `launch.json` to get a full list of predefined variables.


# Dev Containers

Python + Poetry + Jupyter + Extensions

```json
// For format details, see https://aka.ms/devcontainer.json. For config options, see the
// README at: https://github.com/devcontainers/templates/tree/main/src/python
{
    "name": "Python 3",
    // Or use a Dockerfile or Docker Compose file. More info: https://containers.dev/guide/dockerfile
    "image": "mcr.microsoft.com/devcontainers/python:1-3.12-bullseye",
    "features": {
        "ghcr.io/devcontainers-contrib/features/poetry:2": {}
    },
    // Use 'forwardPorts' to make a list of ports inside the container available locally.
    // "forwardPorts": [],
    // Use 'postCreateCommand' to run commands after the container is created.
    "postCreateCommand": "poetry config virtualenvs.in-project true && poetry install && poetry shell",
    // Configure tool-specific properties.
    "customizations": {
        "vscode": {
            "extensions": [
                "charliermarsh.ruff",
                "mechatroner.rainbow-csv",
                "ms-toolsai.jupyter",
                "ms-toolsai.datawrangler",
                "ms-python.python"
            ],
            "vscode": {
                "settings": {
                    "[python]": {
                        "editor.defaultFormatter": "charliermarsh.ruff",
                        "editor.codeActionsOnSave": {
                            "source.fixAll": "explicit",
                            "source.organizeImports": "explicit"
                        }
                    },
                    "python.analysis.fixAll": [
                        "source.unusedImports"
                    ],
                    "editor.formatOnSave": true
                }
            }
        }
    }

    // Uncomment to connect as root instead. More info: https://aka.ms/dev-containers-non-root.

    // "remoteUser": "root"

}
```

