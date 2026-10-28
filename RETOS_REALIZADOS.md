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

