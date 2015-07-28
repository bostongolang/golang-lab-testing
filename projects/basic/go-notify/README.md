# go-notify

## Overview

`go-notify` is a Go package that enables independent components of an application to observe notable events in a decoupled fashion.

Please see the [readme](https://github.com/bitly/go-notify) for an example of its usage.

## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/bitly/go-notify](https://github.com/bitly/go-notify).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path 

```
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/go-notify.git
cd go-notify
```

1. :star2: There are no tests yet, so create an empty file called `notify_test.go` that looks like the following:

```
$ cat notify_test.go
package notify
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
go-notify (master*) $ go test -v notify_test.go
testing: warning: no tests to run
PASS
ok    command-line-arguments  0.005s
```

  * :question: If you need help getting the project tests to run, ask your TA.

