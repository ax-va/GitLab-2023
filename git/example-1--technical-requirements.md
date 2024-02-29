```unix
$ git --version
```
```unix
git version 2.34.1
```

```unix
$ git config --list
```
```unix
user.name=<user_name>
user.email=<user_email>
core.autocrlf=input
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```

```unix
$ git config --global user.email "george.spelvin@example.com"
$ git config --global user.name "George Spelvin"
```

```unix
$ git config --list
```
```unix
user.name=George Spelvin
user.email=george.spelvin@example.com
core.autocrlf=input
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```

Recommended to use "main" instead of "master":
```unix
$ git config --global init.defaultBranch main
```

```unix
$ git config --list
```
```unix
user.name=<user_name>
user.email=<user_email>
core.autocrlf=input
init.defaultbranch=main
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```