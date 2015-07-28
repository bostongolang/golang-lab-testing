# gocsv 

## Overview

`gocsv` is a parser for CSV files. 

## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/mabetle/gocsv](https://github.com/mabetle/gocsv).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/gocsv.git
cd gocsv
```


1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
gocsv (master) $ go test -v . 
=== RUN TestParse
[ID UserName Email RealName Age]
[1 1 1 1 1]
[a a a a a]
[2 demo demo@demo.com Demo测试 33]
[ID UserName Email RealName Age]
Columns:  5
Rows:  3
Row 2:  [2 demo demo@demo.com Demo测试 33]
Row 2,Column 2:  demo@demo.com
--- PASS: TestParse (0.00s)
PASS
ok    github.com/mabetle/gocsv  0.006s
```

  * :question: If you need help getting the project tests to run, ask your TA.

