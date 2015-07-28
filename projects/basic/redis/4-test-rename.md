# Verify Rename() renames a key

*Difficulty Level: Medium*

1. :star2:  In `redis_test.go`, create a `TestRenameChangesKey` function to test the renaming of a key.

```
func TestRenameChangesKey() {
  // TODO your test code here  
}
```

1. :star2: `Flush` the db and verify no error is returned.

1. :star2: In `TestRenameChangesKey`, use the `Set` command to write some data to the "hello-world" key (see [example](https://github.com/hoisie/redis/blob/master/redis_test.go#L33-L37)). Verify no error is returned.

1. :star2: Call `client.Rename("hello-world", "goodbye-world")` to rename hello-world to goodbye-world (code [here](https://github.com/hoisie/redis/blob/master/redis.go#L404-L410)) and verify that no error is returned.

1. :star2: Use the `Get()` command to verify that "goodbye-world" exists 



