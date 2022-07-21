# Clase 05

## Trabajar en proyectos Open Source (Pull Request)

1. Hacer un fork del proyecto. (Me copia el repo a mi cuenta de github)
2. Clono el fork desde mi cuenta GitHub
3. Trabajo normalmente. Subo los cambios
4. Voy al proyecto original en el apartado Pull Request. Creo uno nuevo
5. Una vez aceptado, tendré que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la URL del repositorio.
7. Agrego la URL del repositorio original a mi repositorio local.

    git remote upstream <URL-repositorio-original>

8. Traigo los cambios

    git pull upstream <rama-que-quiero-bajar>

9. Subir actualizaciones del repositorio local a mi remoto.

## TAG (Etiquetado)
Me permite etiquetar commits.

> Ver tags disponibles

    git tag

> Crear un tag en el commit actual

    git tag v1.1

> Crear un tag en un commit específico

    git tag v1.1 <hash>
    git tag v1.1 25fc265

> Generalmente, se usan los tags con versionado semantico

    git tag -a v0.8.0 <hash> -m "Versión 0.1.0"
    git tag -a v0.8.0 d21e942 -m "Versión 0.1.0"

a: anotado
m: mensaje

> Muestra información detallada de los tags

    git show v0.8.0

> Borrar el tag

    git tag -d v0.8.0

> Subir TODOS los tags (no recomendable)

    git push --tags

> Subir un tag en específico

    git push origin <nombre-tag>

## GIT REBASE
Ordena los commits y los fusiona. Tengo que estar sobre la rama master y hacer el git rebase.

    git rebase <rama-que-quiero-traer>
    git rebase <dev>

> Si tengo varios commits

    git rebase --continue

## GIT REBASE INTERACTIVO

> ¿Para qué sirve?

* Ordenar commits
* Corregir mensajes de los commits
* Unir commits
* Separar commits

    git rebase -i HEAD-4
    git rebase -i <HASH>

## Apuntadores

> Apuntadores dinamicos

* HEAD

> Apuntadores estaticos

* RAMAS
* TAG
* STASH

## GIT REFLOG: LA HISTORIA DE LA HISTORIA DE GIT
Tengo toda la interacción con el repositorio de git

    git reflog