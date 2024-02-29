In ~/PycharmProjects:
```unix
$ mkdir test-repo
~/PycharmProjects$ cd test-repo
```

```unix
~/PycharmProjects/test-repo$ git status
Auf Branch master

Noch keine Commits

Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
	../../.bash_history
	../../.bash_logout
...

nichts zum Commit vorgemerkt, aber es gibt unversionierte Dateien
(benutzen Sie "git add" zum Versionieren)
```

```unix
~/PycharmProjects/test-repo$ git init
Leeres Git-Repository in /home/delorian/PycharmProjects/test-repo/.git/ initialisiert
```

```unix
~/PycharmProjects/test-repo$ git init
Bestehendes Git-Repository in /home/delorian/PycharmProjects/test-repo/.git/ neuinitialisiert
```

```unix
~/PycharmProjects/test-repo$ git status
Auf Branch master

Noch keine Commits

nichts zu committen (erstellen/kopieren Sie Dateien und benutzen
Sie "git add" zum Versionieren)
```

Create a file:
```unix
~/PycharmProjects/test-repo$ > todo.txt
```

Stage a file (add to the staging area):
```unix
~/PycharmProjects/test-repo$ git add todo.txt
```

```unix
~/PycharmProjects/test-repo$ git status
Auf Branch main

Noch keine Commits

Zum Commit vorgemerkte Änderungen:
  (benutzen Sie "git rm --cached <Datei>..." zum Entfernen aus der Staging-Area)
        neue Datei:     todo.txt
```

Commit:
```unix
~/PycharmProjects/test-repo$ git commit --message "add empty file"
[main (Root-Commit) d9f6109] add empty file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 todo.txt
```

```unix
 ~/PycharmProjects/test-repo$ git status
Auf Branch main
nichts zu committen, Arbeitsverzeichnis unverändert

~/PycharmProjects/test-repo$ git add todo.txt
~/PycharmProjects/test-repo$ git commit --message "second commit: add first item todo"
[main 18f3c6a] second commit: add first item todo
 1 file changed, 1 insertion(+)
```

~/PycharmProjects/test-repo$ git
```unix
commit 18f3c6ad7690ad36251a287978d2bb1153a6008c (HEAD -> main)
Author: ax-va <my_email>
Date:   Wed Jan 31 08:47:44 2024 +0100

    second commit: add first item todo

commit d9f61092223744979529659f1e1bddefd8be45b2
Author: ax-va <my_email>
Date:   Tue Jan 30 19:11:41 2024 +0100

    add empty file

```

Press "q" to exit.
d9f61092223744979529659f1e1bddefd8be45b2 is a Secure Hash Algorithm (SHA).

Create a file and a directory that will be ignored:
```unix
~/PycharmProjects/test-repo$ > personal-notes.txt
~/PycharmProjects/test-repo$ mkdir ide-config
~/PycharmProjects/test-repo$ cd ide-config
~/PycharmProjects/test-repo/ide-config$ > settings.cnf
~/PycharmProjects/test-repo/ide-config$ cd ..
Auf Branch main
Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
        ide-config/
        personal-notes.txt

nichts zum Commit vorgemerkt, aber es gibt unversionierte Dateien
(benutzen Sie "git add" zum Versionieren)
```

Create .gitignore:
```unix
~/PycharmProjects/test-repo$ nano .gitignore
```

Edit:
// notes to myself that are not for public consumption

`personal-notes.txt`

// configuration files for my IDE

`ide-config/`

`CTRL+O` to save, `CTRL+X` to exit

```unix
~/PycharmProjects/test-repo$ ls -a
.  ..  .git  .gitignore  ide-config  personal-notes.txt  todo.txt

~/PycharmProjects/test-repo$ git add .gitignore
~/PycharmProjects/test-repo$ git commit --message "exclude notes file and IDE config directory"
[main aef47aa] exclude notes file and IDE config directory
 1 file changed, 5 insertions(+)
 create mode 100644 .gitignore
```

```unix
~/PycharmProjects/test-repo$ git status
Auf Branch main
nichts zu committen, Arbeitsverzeichnis unverändert
```