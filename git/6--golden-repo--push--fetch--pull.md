Get a list of remotes that Git knows about
```unix
~/test-repo$ git remote --verbose
```

Create a connection with GitHub to clone the golden repo

Generate SSH keypair:
```unix
$ ssh-keygen -o -t rsa -C "ssh@github.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/delorian/.ssh/id_rsa):
Enter passphrase (empty for no passphrase): ...
Enter same passphrase again: ...
Your identification has been saved in /home/delorian/.ssh/id_rsa
Your public key has been saved in /home/delorian/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:...
The key's randomart image is:
...
```

```unix
$ cd /home/delorian/.ssh/
~/.ssh$ ls
id_rsa  id_rsa.pub  known_hosts
```

Add the given SSH public key on the GitHub's side:
```unix
~/.ssh$ cat id_rsa.pub
ssh-rsa ... ssh@github.com
```

```unix
$ git clone git@github.com:ax-va/Test-for-Git.git
Klone nach 'Test-for-Git' …
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names

----------------------------------------------------

Verify the fingerprint on
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints

    These are GitHub's public key fingerprints:
        SHA256:uNiVztksCsDhcc0u9e8BujQXVUpKZIDTMczCvj3tD2s (RSA)
        SHA256:br9IjFspm1vxR3iA35FWE+4VTyz1hYVLIE2t1/CeyWQ (DSA - deprecated)
        SHA256:p2QAMXNIC1TJYWeIOttrVc98/R1BUFWu3/LiyKgUfQM (ECDSA)
        SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU (Ed25519)

and answer "yes" ONLY IF you found it

----------------------------------------------------

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Enter passphrase for key '/home/delorian/.ssh/id_rsa': ...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Empfange Objekte: 100% (3/3), fertig.
```

```unix
$ cd Test-for-Git
```

```unix
Get a list of remotes that Git knows about
~/Test-for-Git$ git remote --verbose
origin  git@github.com:ax-va/Test-for-Git.git (fetch)
origin  git@github.com:ax-va/Test-for-Git.git (push)
```

"fetch" is for getting other people’s commits,
"push" is for sending my commits.


## pushing

Create a new branch:
```unix
~/Test-for-Git$ git branch new-todos
```

Switch to the new branch:
```unix
~/test-repo$ git switch new-todos
Zu Zweig »new-todos« gewechselt
```

Create a file:
```unix
~/Test-for-Git$ > new-todo.txt
```

Stage a file:
```unix
~/Test-for-Git$ git add new-todo.txt
```

Get the status:
```unix
~/Test-for-Git$ git status
Auf Branch new-todos
Zum Commit vorgemerkte Änderungen:
  (benutzen Sie "git restore --staged <Datei>..." zum Entfernen aus der Staging-Area)
        neue Datei:     new-todo.txt
```

Commit:
```unix
~/Test-for-Git$ git commit --message "new-todo.txt added"
[new-todos 1a1ee58] new-todo.txt added
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 new-todo.txt
```

Get the status:
```unix
~/Test-for-Git$ git status
Auf Branch new-todos
nichts zu committen, Arbeitsverzeichnis unverändert
```

Push the changes into the remote repo,
the name of the remote branch is set once,
then you can use "git push" without the branch's name:
```unix
~/Test-for-Git$ git push --set-upstream origin new-todos
Enter passphrase for key '/home/delorian/.ssh/id_rsa': ...
Objekte aufzählen: 4, fertig.
Zähle Objekte: 100% (4/4), fertig.
Delta-Kompression verwendet bis zu 8 Threads.
Komprimiere Objekte: 100% (2/2), fertig.
Schreibe Objekte: 100% (3/3), 289 Bytes | 289.00 KiB/s, fertig.
Gesamt 3 (Delta 0), Wiederverwendet 0 (Delta 0), Pack wiederverwendet 0
remote:
remote: Create a pull request for 'new-todos' on GitHub by visiting:
remote:      https://github.com/ax-va/Test-for-Git/pull/new/new-todos
remote:
To github.com:ax-va/Test-for-Git.git
 * [new branch]      new-todos -> new-todos
Branch 'new-todos' folgt nun Remote-Branch 'new-todos' von 'origin'
```

## fetching

"git fetch" does not update any branches or files on your local computer.
It collects metadata about any edits without making any changes to your local repo.


## pulling

The file is empty
```unix
~/Test-for-Git$ cat new-todo.txt
```

Change the content and commit on GitHub

```unix
~/Test-for-Git$ git switch new-todos
Bereits auf 'new-todos'
Ihr Branch ist auf demselben Stand wie 'origin/new-todos'.
```

```unix
~/Test-for-Git$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Entpacke Objekte: 100% (3/3), 967 Bytes | 967.00 KiB/s, fertig.
Von github.com:ax-va/Test-for-Git
   1a1ee58..f97c502  new-todos  -> origin/new-todos
Aktualisiere 1a1ee58..f97c502
Fast-forward
 new-todo.txt | 1 +
 1 file changed, 1 insertion(+)
```

```unix
~/Test-for-Git$ cat new-todo.txt
The new content was added
```