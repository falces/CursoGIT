# Conceptos

Control de versiones

Repositorio

Commit

Stagin area

# Instalación

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

Histórico de acciones:

```bash
$ git reflog
```

```
a276a63 (HEAD -> master, origin/master) HEAD@{0}: commit (initial): ADD: Readme
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

```bash:
$ git push
```

