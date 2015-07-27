# Test Start Notify 

*Difficulty Level: Easy*

:star2: Create a test `TestStartNotify`.

```go
func TestStartNotify(t * testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1. :star2: Create a notify channel called `myEventChan` (`myEventChan := make(chan interface{})`).  
   
   :start: Supply this to `notify.Start` with an event name of `my_event` (See code [here](https://github.com/bitly/go-notify/blob/master/notify.go#L50-L55)).

   :star2: Verify the 'events' map ([code](https://github.com/bitly/go-notify/blob/master/notify.go#L44)) has an entry for `my_event`. 

