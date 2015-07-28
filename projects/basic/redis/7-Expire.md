# Write a test to make sure `Expire()` expires keys after 1 second 

*Difficulty Level: Medium*

The goal of this test is to ensure that Expire() set on a key will expire the key (See [http://redis.io/commands/expire](http://redis.io/commands/expire))

1. :star2: In `redis_test.go`, create a test `TestExpire`:

```go
func TestExpire() {
  // todo your test code here  
}
```

1. :star2: In `TestExpire`, use the `Get` command to write some data to the 'expire-me' key (see [example](https://github.com/hoisie/redis/blob/master/redis_test.go#l33-l37)). 
  Verify no error is returned.

1. :star2: In the same method, call `client.Expire` ([code](https://github.com/hoisie/redis/blob/master/redis.go#L429-L437)) on the 'expire-me' key with a timeout of 1 second. 
Verify no error is returned, and that true is returned from the result.

1. :star2: Sleep for 1 second.

1. :star2: Verify that the `Get` command on the 'expire-me' key returns an error.
