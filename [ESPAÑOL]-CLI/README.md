# GITHUB CLI CHEAT SHEET

La interfaz de línea de comandos (CLI) de Git es una herramienta poderosa utilizada para el control de versiones, que permite a los desarrolladores gestionar su código fuente de manera eficiente.

## GITHUB PULL REWESTS

```sh
# Mostrar el estado de las pull requests pertinentes.
gh pr status
```

```sh
# Listar pull request abiertos en repo.
gh pr list
```

```sh
# Listar todos los pull request abiertos en el repositorio.
gh pr list -s all
```

```sh
# Ver un pull request.
gh pr view [<number> | <url> | <branch>]
```

```sh
# Comprobar poner un pull request en Git.
gh pr checkout
```

```sh
# Crear un nuevo pull request.
gh pr create —t <title> —b <body>
```

## GITHUB ISSUES

```sh
# Mostrar el estado de los asuntos relevantes.
gh issue status
```

```sh
# Lista de issues abiertas en el repositorio.
gh issue list
```

```sh
# Lista todas las issues abiertas.
gh issue list —s all
```

```sh
# Ver detalles de una issue.
gh issue view [<number> | <url>]
```

```sh
# Crear una issue
gh issue create —t <title> —b <body>
```

## GITHUB REPOSITORIES

```sh
# 
gh repo clone <repository>
```

```sh
# 
gh repo create <name>
```

```sh
# 
gh repo fork <repository>
```

```sh
# 
gh repo view <repository>
```

## Github command help

```sh
# Muestra la versión de Github CLI
gh --version
```

```sh
# Muestra el template de ayuda.
gh help
```

```sh
# Mostrar información de ayuda para un grupo de comandos específico.
gh <pr | issue | repo> --help
```

```sh
# Mostrar información de ayuda de un comando específico.
gh <pr | issue | repo> <comand> --help
```
