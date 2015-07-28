# Write a test for Randomkey() 

*Difficulty Level: Easy*

`Randomkey()` ([Redis API docs](http://redis.io/commands/RANDOMKEY)) should return a random key. 

1. :star2:  In `redis_test.go`, create a `TestRandomkey` function.  

```
func TestRandomkey() {
  // TODO your test code here  
}
```

1. :star2: `Flush` the db and verify no error is returned.

1. :star2: In `TestRandomkey`, use the `Set` command to write some data (see [example](https://github.com/hoisie/redis/blob/master/redis_test.go#L33-L37)). Verify no error is returned.

1. :star2: Call `client.Randomkey()` (code [here](https://github.com/hoisie/redis/blob/master/redis.go#L396-L402)) and verify that no error is returned, and the row you inserted in the previous 
step is found.

