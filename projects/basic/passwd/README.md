# passwd

## Overview

`passwd` is a Go package that parses /etc/passwd files, see example [passwd](example_passwd)).

## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/willdonnelly/passwd](https://github.com/willdonnelly/passwd).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/passwd.git
cd `passwd`
```

1. :star2: There are no tests yet, so create an empty file called `passwd_test.go` that looks like the following:

```
$ cat passwd_test.go
package passwd
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
passwd (master*) $ go test -v .
testing: warning: no tests to run
PASS
ok    github.com/willdonnelly/passwd  0.007s
```

  * :question: If you need help getting the project tests to run, ask your TA.

