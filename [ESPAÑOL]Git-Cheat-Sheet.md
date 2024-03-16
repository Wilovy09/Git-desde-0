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
# Inicializa un directorio existente como repositorio Git.
git init
```

```sh
# Recupera un repositorio completo desde una ubicación alojada mediante URL.
git clone [url]
```

## Stage & Snapshot

Trabajar con instantáneas y el área de preparación de Git.

```sh
# Mostrar los archivos modificados en el directorio de trabajo, preparados para su próxima confirmación.
git status
```

```sh
# Añadir un archivo tal y como se ve ahora a su próxima confirmación (etapa).
git add [file]
```

```sh
# Desmontar un fichero conservando los cambios en el directorio de trabajo.
git reset [file]
```

```sh
# Acantilado de lo que se cambia pero no se escenifica.
git diff
```

```sh
# Diff de lo que está preparado pero aún no comprometido.
git diff --staged
```

```sh
# Confirmar el contenido preparado como una nueva instantánea de confirmación.
git commit -m “[descriptive message]”
```

## Branch & Merge

Aislar el trabajo en ramas, cambiar el contexto e integrar los cambios.

```sh
# Enumere sus sucursales. Aparecerá un * junto a la rama activa en ese momento.
git branch
```

```sh
# Crear una nueva rama en el commit actual.
git branch [branch-name]
```

```sh
# Cambia a otra rama y compruébalo en tu directorio de trabajo.
git checkout
```

```sh
# Fusionar el historial de la rama especificada en la actual.
git merge [branch]
```

```sh
# Mostrar todos los commits en el historial de la rama actual.
git log
```

## Inspect & Compare

Examinar logs, diffs e información sobre objetos.

```sh
# Mostrar el historial de confirmaciones de la rama activa en ese momento.
git log
```

```sh
# Mostrar los commits de la ramaA que no están en la ramaB.
git log branchB..branchA
```

```sh
# Mostrar los commits que cambiaron el archivo, incluso a través de renombramientos.
git log --follow [file]
```

```sh
# Mostrar la diferencia entre lo que está en la ramaA y lo que no está en la ramaB.
git diff branchB...branchA
```

```sh
# Mostrar cualquier objeto en Git en formato legible por humanos.
git show [SHA]
```

## Share & Update

Recuperación de actualizaciones de otro repositorio y actualización de los repos locales.

```sh
# Añade una URL git como alias.
git remote add [alias] [url]
```

```sh
# Obtener todas las ramas de ese Git remoto.
git fetch [alias]
```

```sh
# Fusionar una rama remota en su rama actual para actualizarla.
git merge [alias]/[branch]
```

```sh
# Transmitir los commits de la rama local a la rama del repositorio remoto.
git push [alias] [branch]
```

```sh
# Obtener y fusionar los commits de la rama remota de seguimiento
git pull
```

## Tracking Path Changes

Versionado de archivos eliminados y cambios de ruta.

```sh
# Eliminar el archivo del proyecto y preparar la eliminación para la confirmación.
git rm [file]
```

```sh
# Cambie la ruta de un archivo existente y escenifique el movimiento.
git mv [existing-path] [new-path]
```

```sh
# Mostrar todos los registros de confirmación con indicación de las rutas que se han movido.
git log --stat -M
```

## Rewrite history

Reescribir ramas, actualizar commits y borrar el historial.

```sh
# Aplica cualquier confirmación de la rama actual por delante de la especificada.
git rebase [branch]
```

```sh
# Limpia el área de preparación, reescribe el árbol de trabajo desde la confirmación especificada.
git reset --hard [commit]
```

## Temporary commits

Almacenar temporalmente los archivos modificados y rastreados para cambiar de rama.

```sh
# Guardar los cambios modificados y por etapas.
git stash
```

```sh
# Listar el orden de pila de los cambios de archivo almacenados.
git stash list
```

```sh
# Escribir trabajando desde la parte superior de la pila de alijo.
git stash pop
```

```sh
# Descarta los cambios de la parte superior de la pila de alijo.
git stash drop
```

## Ignoring patherns

Evitar la puesta a disposición o la consignación involuntaria de archivos.

```txt
logs/
*.notes
pattern*/

# Guarde un archivo con los paterns deseados como .gitignore ya sea con coincidencias directas de cadena
o comodines.
```

```sh
# Patern ignorado en todo el sistema para todos los repositorios locales.
git config --global core.excludesfile [file]
```
