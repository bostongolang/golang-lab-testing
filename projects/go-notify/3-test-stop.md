# Test Stop Notify 

*Difficulty Level: Easy*

:star2: Create a test `TestStopNotify`.

```go
func TestStopNotify(t * testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1. :star2: Create a notify channel called `myEventChan` (`myEventChan := make(chan interface{})`).  
   Supply this to `notify.Start` with an event name of `my_event`.

   :star2: Run `notify.Stop` ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L58-L77)) for `my_event` and `myEventChan` 
   and verify it returns no error.

   :star2: Verify the 'events' map ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L44)) is empty.

1. :star2: Call `notify.Start` with an event name of `my_event_two`.

   :star2: Run `notify.StopAll("my_event_two")` ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L80-L94)) and verify it returns no error. 

   :star2: Verify the 'events' map ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L44)) is empty.

1. :star2: Run `notify.StopAll("non_existent_event")` and verify it returns an `E_NOT_FOUND` error (see [code](https://github.com/bitly/go-notify/blob/master/notify.go#L86)).

