# Verify Renamenx() renames a key if it doesn't exist.

*Difficulty Level: Medium*

Renamenx renames a key if it doesn't exist.  Redis docs are [here](http://redis.io/commands/renamenx).

1. :star2:  In `redis_test.go`, create a `TestRenamenxChangesKey` function to test the renaming of a key.  Code is [here](https://github.com/hoisie/redis/blob/master/redis.go#L412-L418)

```
func TestRenamenxChangesKey() {
  // TODO your test code here  
}

```

1. :star2: `Flush` the db and verify no error is returned.

1. :star2: In `TestRenamenxChangesKey`, use the `Set` command to write some data to the "hello-world" key (see [example](https://github.com/hoisie/redis/blob/master/redis_test.go#L33-L37)). Verify no error is returned.

1. :star2: In the same function, call `client.Renamenx("hello-world", "goodbye-world")` to rename hello-world to goodbye-world 
(code [here](https://github.com/hoisie/redis/blob/master/redis.go#L404-L410)) and verify that no error is returned, and that "true" is returned from the result.

1. :star2: In the same function, use the `Get()` command to verify that "goodbye-world" exists.

1. :star2: In the same function, write some data to the "hello-world" key using the `Set` command.

1. :star2: In the same function, call `client.Renamenx("hello-world", "goodbye-world")` to rename hello-world to goodbye-world 
(code [here](https://github.com/hoisie/redis/blob/master/redis.go#L404-L410)) and verify that no error is returned, and that "false" is returned from the result. (It should be false because the key
already exists).




