- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

    git reset --hard HEAD~1

    Porque con este comando podemos deshacer el último commit dentro de la rama en la que estamos. 
    También se pierden los cambios en working copy y stanging area queda vacio.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

    git reflog

    Utilice el comando para ver todo lo que ha sucedido en el repositorio y en en orden del más actual al más antiguo.
    En este listado copiamos el id del commit que nos interesa.

    git reset --hard 356e4e1

    Para poder restablecer el commit que deshicimos en la rama en la que estamos.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

    git merge main

    Con este comando realizamos un merge (fusión) sobre la rama main, es decir la rama en la que estamos (styled) absorve a la que mencionamos (main).

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

    Si, porque los cambios que realizamos desde la rama "htmlify" fueron desde el fichero que se trajo de la rama "main". 
    Este fichero no tiene los útlimos cambios que se realizarón en la rama "styled" dado que fue main fue absorvida por "styled" y no viceversa.
    Y por lo tanto tienen cambios a la vez en el mismo fichero y en algunas líneas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

    No porque el fichero que contiene la rama de "main" tiene los cambios originales del fichero que se encuentra en la rama "styled", así que puede absorver los nuevos cambios.

- ¿Qué comando o comandos utilizaste en el paso 25?

    git log --graph --decorate --pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

    Si porque mientras hicimos los cambios en la rama "title" no se realizaron commits desde la rama "main", es decir el último commit en la rama "main" fue antes del commit en la rama "title".

- ¿Qué comando o comandos utilizaste en el paso 27?

    git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?

    git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?

    git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?

    git reflog
    git checkout c8739cc    (es el id del commit perdido por la rama borrada)
    git branch title
    git checkout title
    cat git-nuestro         (confirmamos que tenemos nuestros cambios en el fichero)
    git checkout main
    git merge --no-ff title

- ¿Qué comando o comandos usaste en el paso 32?

    git reflog
    git checkout 9e85f19    (es el id del commit inicial)

- ¿Qué comando o comandos usaste en el punto 33?

    git log
    git checkout c8739ccea83e5cc38550658a99da9910c5abb7fe
