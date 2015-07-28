# Write a test for Flush() and Keys()

*Difficulty Level: Medium*

1. :star2:  In `redis_test.go`, create a test `TestFlushReturnsNoKeys` 

```
func TestFlushReturnsNoKeys() {
  // TODO your test code here  
}
```

1. :star2: In `TestFlushReturnsNoKeys`, use the `Set` command to write some data to the "test-flush" key (see [example](https://github.com/hoisie/redis/blob/master/redis_test.go#L33-L37)). Verify no error is returned.

1. :star2: In the same method, call `client.Flush(false)` (code [here](https://github.com/hoisie/redis/blob/master/redis.go#L458-L470)) and verify that no error is returned. 

1. :star2: In the same method, call `client.Keys()` and verify no data is returned and no error is returned (code is [here](https://github.com/hoisie/redis/blob/master/redis.go#L374-L394)). 
