Add a tag representing the version number to the latest commit on your branch:
```unix
~/test-repo$ git tag version-1-0-beta
```

```unix
~/test-repo$ git log

commit aef47aa16386bdf99399df2b57250703d752a378 (HEAD -> main, tag: version-1-0-beta)
Author: ax-va <my_email>
Date:   Wed Jan 31 19:42:08 2024 +0100

    exclude notes file and IDE config directory

commit 18f3c6ad7690ad36251a287978d2bb1153a6008c
Author: ax-va <my_email>
Date:   Wed Jan 31 08:47:44 2024 +0100

    second commit: add first item todo

commit d9f61092223744979529659f1e1bddefd8be45b2
Author: ax-va <my_email>
Date:   Tue Jan 30 19:11:41 2024 +0100
```

```unix
~/test-repo$ git tag --list
version-1-0-beta
```

```unix
~/test-repo$ git tag --delete version-1-0-beta
Tag 'version-1-0-beta' gelöscht (war aef47aa)
```

```unix
~/test-repo$ git tag --list
<empty list>
```