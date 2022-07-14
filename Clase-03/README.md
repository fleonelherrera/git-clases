# CLASE 03

## GIT BRANCH

> Permite crear ramas, recibe como parametro el nombre de la rama

    git branch <nombre-rama>
    git branch rama2

> Ver ramas en el repo

    git branch

> Cambiar de rama

    git switch <nombre-rama>
    git switch rama2

> Borrar una rama

    git branch -d <nombre-rama>
    git branch -d rama2


## GIT MERGE (fusiones de ramas)

**IMPORTANTE**: Siempre tengo que estar en la rama que quiero recibir los cambios. Si quiero traerme a **master** lo que tengo en **dev**, tengo que estar posicionado sobre la rama **master**.

> estando en MASTER hago una fusión de ramas con rama2.

    git merge <nombre-rama>
    git merge rama2

### TIPOS DE MERGE (tipos de fusiones)

* Fast-Fodward: No hay ningún conflicto, se hace de manera automática.

* Recursivo (Uniones automaticas): No hay conflictos, trabaja con un algoritmo.

* Manual: Hay conflictos, los integrantes del equipo deben juntarse para resolver los problemas.