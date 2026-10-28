# Retos extra de Git

**Participante:** Jimena
**Rama de trabajo:** `jimena/retos-extra`
**Repositorio:** `aleflcc/practica6`

## Reto 1 — Detective del historial

### 1. Consultar el historial de ramas

Comando ejecutado:

`git log --oneline --graph --decorate --all`

**Aprendizaje:** permite visualizar los commits y las relaciones entre las ramas, incluyendo las referencias de las ramas locales y remotas.

### 2. Inspeccionar el último commit

Comando ejecutado:

`git show HEAD`

**Aprendizaje:** muestra los datos del commit señalado por `HEAD`, incluyendo su autor, fecha, mensaje y cambios.

### 3. Comparar cambios sin preparar
Comando ejecutado:

`git diff`

**Demostración:** se utilizó un archivo de prueba temporal. El resultado mostró el cambio de `Estado inicial` a `Estado modificado`.

**Aprendizaje:** compara los cambios del directorio de trabajo con el área de preparación.

### 4. Comparar cambios preparados

Comando ejecutado:

`git diff --staged`

**Demostración:** mostró la creación del archivo de prueba con el contenido `Estado inicial`, que se había preparado con `git add`.

**Aprendizaje:** compara los cambios preparados con la versión registrada en el último commit.

### 5. Consultar la historia de un archivo

Comando ejecutado:

`git blame panel/estado.md`

**Demostración:** se identificaron los commits asociados a las líneas del archivo, junto con sus autores y fechas.

**Aprendizaje:** permite rastrear el historial de las líneas de un archivo y comprender de qué cambios provienen.

### Limpieza

Se retiró del área de preparación y se eliminó el archivo temporal `prueba_reto1.txt`. Se comprobó que el directorio de trabajo quedó limpio antes de preparar este registro.


## Reto 2 — Saltos y rescates

### 1. Regresar a la rama anterior

Comando ejecutado:

`git switch -`

**Aprendizaje:** permite regresar a la rama visitada anteriormente. Después se volvió a `jimena/retos-extra`.

### 2. Guardar temporalmente cambios

Comandos ejecutados:

`git stash push -m "pausa de mision"`
`git stash list`
`git stash pop`

**Demostración:** se utilizó un archivo temporal preparado previamente con `git add`. Se guardó el cambio, se consultó el stash y después se recuperó.

**Aprendizaje:** `git stash` permite apartar temporalmente cambios sin crear un commit. `git stash list` muestra las entradas guardadas y `git stash pop` recupera una entrada y la elimina de la lista si la operación termina correctamente.

### 3. Consultar movimientos recientes

Comando ejecutado:

`git reflog`

**Aprendizaje:** muestra los movimientos recientes de `HEAD`, incluidos cambios de rama y commits.

### 4. Actualizar referencias remotas

Comando ejecutado:

`git fetch origin`

**Aprendizaje:** actualiza la información de las ramas remotas sin fusionar sus cambios en la rama actual.

### 5. Comparar la rama con develop

Comando ejecutado:

`git diff origin/develop...HEAD`

**Demostración:** se identificaron los archivos que difieren entre la rama de trabajo y `origin/develop`.

**Aprendizaje:** permite revisar los cambios de una rama desde el punto común de sus historiales.

### 6. Restaurar un archivo

Comando ejecutado:

`git restore -- manual/comandos.md`

**Aprendizaje:** restaura el archivo a su versión registrada en el índice. Se comprobó previamente que no hubiera cambios pendientes en ese archivo, por lo que no se descartó trabajo.
