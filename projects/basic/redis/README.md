# redis 

## Overview

`redis` provides a Go client API for redis.  The Redis API is well documented here: [http://redis.io/commands](http://redis.io/commands)

```
package main

import "github.com/hoisie/redis"

func main() {
    var client redis.Client
    var key = "hello"
    client.Set(key, []byte("world"))
    val, _ := client.Get("hello")
    println(key, string(val))
}
```

We'll write some tests that cover API calls not covered in the test suite.


## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/hoisie/redis](https://github.com/hoisie/redis).

  * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

1. :star2: Clone your fork of your repo to your $GOPATH source path.

```bash
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/redis.git
cd redis
```

1. :star2: Run `go get -v .` to install the dependencies for the `redis` package.

1. :star2: In order to run the webserver, you need to have redis installed.  Install redis and make sure it is started and listening on 6379.

```
$ redis-server
~ $ redis-server                                                                                                                            ~ 130 ↵
[24304] 28 Jul 15:47:13.004 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf
[24304] 28 Jul 15:47:13.006 * Max number of open files set to 10032
                _._
           _.-``__ ''-._
      _.-``    `.  `_.  ''-._           Redis 2.6.10 (00000000/0) 64 bit
  .-`` .-```.  ```\/    _.,_ ''-._
 (    '      ,       .-`  | `,    )     Running in stand alone mode
 |`-._`-...-` __...-.``-._|'` _.-'|     Port: 6379
 |    `-._   `._    /     _.-'    |     PID: 24304
  `-._    `-._  `-./  _.-'    _.-'
 |`-._`-._    `-.__.-'    _.-'_.-'|
 |    `-._`-._        _.-'_.-'    |           http://redis.io
  `-._    `-._`-.__.-'_.-'    _.-'
 |`-._`-._    `-.__.-'    _.-'_.-'|
 |    `-._`-._        _.-'_.-'    |
  `-._    `-._`-.__.-'_.-'    _.-'
      `-._    `-.__.-'    _.-'
          `-._        _.-'
              `-.__.-'

[24304] 28 Jul 15:47:13.007 # Server started, Redis version 2.6.10
[24304] 28 Jul 15:47:13.007 * DB loaded from disk: 0.000 seconds
[24304] 28 Jul 15:47:13.007 * The server is now ready to accept connections on port 6379
```

1. :star2: Run `go test -v .` to ensure that the test run.

You should see something like this:

```bash
redis (master) $ go test -v .      
set paste
redis (master) $ go test -v .                                                                                  ~GOPATH/src/github.com/hoisie/redis
=== RUN TestBasic-2
--- PASS: TestBasic-2 (0.00s)
=== RUN TestEmptyGet-2
--- PASS: TestEmptyGet-2 (0.00s)
=== RUN TestConcurrent-2
--- PASS: TestConcurrent-2 (0.00s)
=== RUN TestSet-2
--- PASS: TestSet-2 (0.00s)
=== RUN TestList-2
--- PASS: TestList-2 (0.00s)
=== RUN TestLrem-2
--- PASS: TestLrem-2 (0.00s)
=== RUN TestBrpop-2
--- PASS: TestBrpop-2 (0.00s)
=== RUN TestBlpop-2
--- PASS: TestBlpop-2 (0.00s)
=== RUN TestBrpopTimeout-2
--- PASS: TestBrpopTimeout-2 (1.05s)
=== RUN TestBlpopTimeout-2
--- PASS: TestBlpopTimeout-2 (2.00s)
=== RUN TestSortedSet-2
--- PASS: TestSortedSet-2 (0.01s)
=== RUN TestHash-2
--- PASS: TestHash-2 (0.00s)
=== RUN TestHmset-2
--- PASS: TestHmset-2 (0.00s)
PASS
ok    github.com/hoisie/redis 3.074s
```

  * :question: If you need help getting the project tests to run, ask your TA.

