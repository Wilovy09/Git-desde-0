# Git hoja de comandos

Git es el sistema de control de versiones distribuido, gratuito y de código abierto responsable de todo lo relacionado con GitHub
que ocurre localmente en tu ordenador. Esta hoja de trucos presenta los comandos más importantes y comúnmente
más importantes y utilizados de Git.

## Instalación & gui

Con instaladores específicos de plataforma para Git, GitHub también proporciona la
la facilidad de mantenerse al día con las últimas versiones de la
línea de comandos, a la vez que proporciona una interfaz gráfica de usuario para la interacción
diaria, revisión y sincronización de repositorios.

### Github para Windows

[htps://windows.github.com](htps://windows.github.com)

### Github para Mac

[htps://mac.github.com](htps://mac.github.com)

### Github para todas las plataformas

[htp://git-scm.com](htp://git-scm.com)

## Setup

Configuración de la información de usuario utilizada en todos los repositorios locales.

```sh
# Establece un nombre que sea identificable para el crédito cuando se revise el historial de versiones.
git config --global user.name "[NOMBRE APELLIDO]"
```

```sh
# Establece una dirección de correo electrónico que se asociará a cada marcador del historial.
git config --global user.email "[email-valido]"
```

```sh
# Colorear automáticamente la línea de comandos de Git para facilitar la revisión.
git config --global color.ui auto
```

## Setup & init

Configuración de la información de usuario, inicialización y clonación de repositorios.

```sh
# Inicializa un directorio existente como repositorio Git
git init
```

```sh
# Recupera un repositorio completo desde una ubicación alojada mediante URL.
git clone [url]
```
