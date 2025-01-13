# Not intuitive commands

List all available branches:
```unix
$ git branch
* main
```

Make a new branch with name `foo`:
```unix
$ git branch foo
```

```unix
$ git branch
  foo
* main
```

Deletes a branch called `foo`:
```unix
$ git branch --delete foo
Branch foo entfernt (war 178bb66).
```

```unix
$ git branch
* main
```