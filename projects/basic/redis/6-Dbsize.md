# Verify Dbsize() renames a key if it doesn't exist.

*Difficulty Level: Medium*

1. :star2:  In `redis_test.go`, create a function `TestDbsize`

```
func TestDbsize() {
  // TODO your test code here  
}

```

1. :star2: Call `Flush(false)` to clear the database 

1. :star2: Call `Dbsize` ([code](https://github.com/hoisie/redis/blob/master/redis.go#L420-L427)) and verify an int value == 0 is returned, and no error is returned. 


