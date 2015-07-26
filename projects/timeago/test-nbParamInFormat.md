# Unit Test for `nbParamInFormat` 

`nbParamInFormat` [link to the function here](https://github.com/xeonx/timeago/blob/master/timeago.go#L160-L162)
counts the number of parameters in a format string. 

:star2: Write tests for `nbParamInFormat` that tests the following cases:
  * nbParamInFormat("this has 1 format string %s") => should return 1
  * nbParamInFormat("this has 2 format strings %s %d") => should return 2
  * nbParamInFormat("this has 2 format strings %s %d, the percent %% is escaped") => should return 2

...Any others you can think of?

```go
func TestNbParamInFormat() {
  // YOUR TEST CODE HERE 
}
```
