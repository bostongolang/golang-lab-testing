# Write test clean up function 

*Difficulty Level: Easy*

1. :star2:  In `redis_test.go`, create a function that cleans data by calling `client.Flush(false)`. This will flush all data in the test database. 

The Flush api is [here](https://github.com/hoisie/redis/blob/master/redis.go#L458-L470).
FLUSH redis documents are [here](http://redis.io/commands/FLUSHDB).

```
func FlushData() {
  // TODO your flush code here 
}
```

1. :star2: Verify that no error is returned. 

1. :star2: Ensure this runs in `TestMain` before the test suite is run.

