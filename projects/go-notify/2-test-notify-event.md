# Test Notify Event on Channel

*Difficulty Level: Medium*

:star2: Create a test `TestNotifyEventOnChannel`.

```go
func TestNotifyEventOnChannel(t * testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1. Create a notify channel called `myEventChan` (`myEventChan := make(chan interface{})`).  
   Supply this to `notify.Start` with an event name of `my_event`.

   :star2: Posts an event `hello` using `notify.Post` ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L96-L110)). 
   Verify that `notify.Post` returns no error (you will have to do this in a goroutine).

   :star2: Verify that `hello` is successfully read from the channel after 1 second (you will have to do this in a goroutine).

