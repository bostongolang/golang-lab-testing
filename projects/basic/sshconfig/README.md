# sshconfig

## Overview

`sshconfig` is a Go package that parses ssh configuration files (located in ~/.ssh/config, see example [sshconfig](example_ssh_config)).

## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/dullgiulio/sshconfig](https://github.com/dullgiulio/sshconfig).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/sshconfig.git
cd sshconfig
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
sshconfig (master) $ go test -v .                                                                                  ~GOPATH/src/github.com/dullgiulio/sshconfig
=== RUN TestHostSection
--- PASS: TestHostSection (0.00s)
PASS
ok    github.com/dullgiulio/sshconfig 0.005s
```

  * :question: If you need help getting the project tests to run, ask your TA.

