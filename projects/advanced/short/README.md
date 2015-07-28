# short 

## Overview

`short` is a URL shortener. It runs as webserver that allows you to post URLs to be shortened using the following command:

```
$  curl -d '{"url":"http://example.com"}' http://127.0.0.1:8880    
{"Original":"http://example.com","Short":"B","FullShort":"http://127.0.0.1:8880/B","HitCount":0}%
```


## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/johnnye/short](https://github.com/johnnye/short).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```bash
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/short.git
cd short
```

1. :star2: Run `go get -v .` to install the dependencies for the `short` package.

1. :star2: In order to run the webserver, you need to have redis installed.  Install redis and make sure it is started and listening.

1. :star2: To run the webserver on port `8880`, type the following:

```bash
go run short.go -p 8880 -b http://127.0.0.1:8880/
```

1. :star2: In another terminal window, verify that everything works by using curl:

```bash
$  curl -d '{"url":"http://example.com"}' http://127.0.0.1:8880    
{"Original":"http://example.com","Short":"B","FullShort":"http://127.0.0.1/B","HitCount":0}%
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
short (master) $ go test -v .      
=== RUN TestCreateShortURL
--- PASS: TestCreateShortURL (0.00s)
PASS
ok    github.com/jandre/short 0.007s
```

  * :question: If you need help getting the project tests to run, ask your TA.

