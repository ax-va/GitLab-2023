Create a new branch:
```unix
~/test-repo$ git branch new-features
```

List all branches:
```unix
~/test-repo$ git branch
* main
  new-features
```

Switch to a branch (two commands that do the same):
```unix
~/test-repo$ git checkout new-features
Zu Zweig »new-features« gewechselt
```

```unix
~/test-repo$ git switch main
Zu Zweig »main« gewechselt
```

```unix
~/test-repo$ git switch new-features
Zu Zweig »new-features« gewechselt
```

Merge one branch (called the source branch) into another branch (called the target branch).
Merge "new-features" into "main".

First, make sure you are on the target branch:
```unix
~/test-repo$ git checkout main
Zu Zweig »main« gewechselt
```

Then, perform the merge while specifying the source branch:
```unix
~/test-repo$ git merge new-features
Bereits aktuell.
```

Delete a branch:
```unix
~/test-repo$ git branch --delete new-features
Branch new-features entfernt (war b196005).
```

or

```unix
~/test-repo$ git branch -d new-features
Branch new-features entfernt (war b196005).
```

Force delete:
```unix
~/test-repo$ git branch new-features2
~/test-repo$ git branch --delete --force new-features2
Branch new-features2 entfernt (war b196005).
```
