# Clase 04

## .gitkeep: Versionar carpetas vacías
Creo un archivo vacío llamado .gitkeep dentro de la carpeta que quiero versionar

## Alias
Forma resumida para llamar a un comando

    git config --global alias.l "log --oneline"
    git config --global alias.s "status --short"
    git config --global alias.ll log --oneline --decorate --all --graph

### Ver alias disponibles

    git config --get-regexp alias

### Borrar un alias

    git config --global --unset alias.<nombre-alias>

## GIT STASH
**NOTA** Los stash no estan disponibles en el remoto. Solo localmente. No se pueden subir al remoto.

### Crear un stash

    git stash

### Veo los stash

    git stash list

### Borrar un stash

>Borrar el último stash
    git stash drop

> Borrar un stash en particular

    git stash drop <stash>

> Aplicar un stash, el último

    git stash pop

> Aplicar cualquier stash

    git stash apply
    git stash apply stash@{1}

## GIT RESET

> SOFT: Saca los commits y deja todo en Staging area (add)

    git reset --soft

> MIXED: Saca los commits y los deja en Working Directory (antes del add)

    git reset <numero-hash>
    git reset --mixed

> HARD (peligroso, mucho cuidado): Borra los commits y los cambios definitivamente

    git reset --hard
