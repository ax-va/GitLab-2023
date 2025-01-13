```unix
$ git --version
git version 2.34.1
```

```unix
$ git config --list
user.name=<your_name>
user.email=<your_email>
core.autocrlf=input
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```

```unix
$ git config --global user.email "ax-va@example.com"
$ git config --global user.name "Alexander Vasiliev"
```

```unix
$ git config --list
user.name=Alexander Vasiliev
user.email=ax-va@example.com
core.autocrlf=input
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```

Recommended using `main` instead of `master`:
```unix
$ git config --global init.defaultBranch main
```

```unix
$ git config --list
user.name=<your_name>
user.email=<your_email>
core.autocrlf=input
init.defaultbranch=main
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
```