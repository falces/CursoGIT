# Conceptos

Control de versiones

Repositorio

Commit

Stagin area

# Instalación

## Windows

Descargar el instalador de la página oficial: https://git-scm.com/. Es una instalación sencilla "siguiente...", pero hay que asegurarse de que en las opciones de instalación se instala Git Bash (la terminal de Git).

# Comandos

Inicializar un repositorio en un directorio:

```bash
$ git init
```

Estado de los archivos y repositorio:

```bash
$ git status
```

```
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
```

Mostrar el histórico con los cambios hechos:

```bash
$ git show
```

```
commit a276a6380d030196ddc23533c3f080fa63a8d844 (HEAD -> master, origin/master)
Author: javier.rodriguez <javier.rodriguez@digimobil.es>
Date:   Sat Nov 20 22:39:54 2021 +0100

    ADD: Readme

diff --git a/Readme.md b/Readme.md
new file mode 100644
index 0000000..509f0c9
--- /dev/null
+++ b/Readme.md
@@ -0,0 +1,34 @@
+# Conceptos
+
+Control de versiones
+
+Repositorio
+
+Commit
```

Historia de un archivo:

```bash
# git log [NOMBRE_DE_ARCHIVO]
$ git log mi_archivo
```

```
commit a276a6380d030196ddc23533c3f080fa63a8d844 (HEAD -> master, origin/master)
Author: javier.rodriguez <javier.rodriguez@digimobil.es>
Date:   Sat Nov 20 22:39:54 2021 +0100

    ADD: Readme
```

Histórico de acciones, de más a menos reciente:

```bash
$ git reflog
```

```
7bc16b8 (HEAD -> master, origin/master) HEAD@{0}: commit: WIP: Progress
a276a63 HEAD@{1}: commit (initial): ADD: Readme
```

Añadir un archivo al staging area:

```bash
# git add [NOMBRE_DE_ARCHIVO]
$ git add mi_archivo.txt
```

Añadir todos los archivos modificados al staging area:

```bash
$ git add .
```

Commit de los archivos del staging area:

```bash
# git commit -m "[MENSAJE]"
$ git commit -m "ADD: New files"
```

##  Trabajar con repositorios remotos

Enviar cambios a un repositorio remoto:

```bash
$ git push
```

```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.03 KiB | 16.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:falces/CursoGIT.git
   a276a63..7bc16b8  master -> master
```

Traer cambios de un repositorio remoto:

```bash
$ git pull
```

