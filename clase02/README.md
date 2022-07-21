# Clase 02 - 12/07/2022
# ---------------------

# Status de archivos

* UNTRACKED > Archivos que o se agregaron al index o estan en el working directory

* STAGED > Archivos que no fueron agregados al repositorio y cuyos cambios fueron validados.

* UNMODIFIED > Archivos que se encuentran en el repositorio y que no fueron modificados

* MODIFIED > Archivos que se encuentran en el repositorio pero difieren con lo que se encuentra en el working directory


## GIT LOG

Muestra versión completa

    git log

Muestra versión corta

    git log --oneline

Muestra una cantidad de commit seleccionado

    git log -<cantidad-commit>

    git log -3
    
Busco por fechas

    git log --since="2022-05-01"
    git log --after="2022-07-03"
    git log --before="2022-07-08"

## GITIGNORE

Archivo q nos permite no darle seguimiento a otros

    .gitignore

## GIT COMMIT

    git commit --help

### Sacar una foto o hacer commit. Se abre el editor que hayamos configurado

    git commit

### Para poner un mensaje directamente en consola usamos -m

    git commit -m "mensaje"

### Si quiero directamente hacer un git add y un git commit

**IMPORTANTE**: El archivo tiene que estar dentro del repositorio de git. O sea los archivos UNTRACKED no los agrega a la foto.

    git commit -am "mensaje"

### Crear un commit vacío

    git commit --allow-empty -m "mensaje"

### Agrego algo que me olvidé en el último commit

    git commit --amend

## GIT ADD

### Por archivo

    git add index.html

### Agrego todo

    git add .

### Agrego partes de un archivo 

    git add -p

* y: yes
* n: no

## GIT REMOTE

### Para ver los remotos

    git remote

### Ver remotos en forma detallada

    git remote -v

### Agregar un remoto

    git remote add <alias-remoto> <url>

### Renombrar el remoto

    git remote <nombre-original> <nombre-nuevo>

Ejemplo

    git remote origin franco

### Borrar remoto

    git remote rm <alias-remoto>

