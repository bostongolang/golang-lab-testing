# koala 

## Overview

`koala` is a command line tool that formats file output listings.  

```
$ koala -o lisp
(#P"README.md" #P"koala.go")

$ koala -o space
README.md koala.go

$ koala -o comma
README.md,koala.go

$ koala -o null
README.mdkoala.go
```


## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/gokyle/koala](https://github.com/gokyle/short).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```bash
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/koala.git
cd koala
```

1. :star2: Run `go get -v .` to install the dependencies for the `koala` package.

1. :star2: Run the koala command line tool to make sure it works.

```bash
$ go run koala.go -o comma
LICENSE,README.md,koala.go
```

1. :star2: since no test file is found, create a `koala_test.go` file with the package `main`

```
$ more koala_test.go
package main
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
koala (master) $ go test -v .      
testing: warning: no tests to run
PASS
ok    github.com/jandre/koala 0.005s
```

  * :question: If you need help getting the project tests to run, ask your TA.

