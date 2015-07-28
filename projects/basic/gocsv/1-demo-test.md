# Convert Demo to Test Verification

*Difficulty Level: Easy*

:star2: Open `parse_test.go`. You'll see that it has a function called `TestParse` which runs a `Demo` function. 

```go
// test parse
func TestParse(t *testing.T){

  Demo()

}
```

Currently, this function runs the demo. Let's convert the [Demo function](https://github.com/mabetle/gocsv/blob/master/demo.go#L7-L19) to tests. 

1. :star2: Remove the call to `Demo()`, copy the contents of the Demo function [Demo function](https://github.com/mabetle/gocsv/blob/master/demo.go#L7-L19) to the test function. 

1. :star2: Verify that [GetHeaderRow](https://github.com/mabetle/gocsv/blob/master/demo.go#L12) results match the header in [demo_read.csv](https://github.com/mabetle/gocsv/blob/master/demo_read.csv).

  * Hint: you may have to write a helper function to compare arrays, or maybe look at using `reflect.DeepEqual()`.

1. :star2: Verify that `GetColumns()` returns 5.

1. :star2: Verify that `GetRows()` returns 3.

1. :star2: Verify that `GetRow(2)` returns the correct values for the second row.

1. :star2: Verify that `GetString(2,2)` returns `demo@demo.com` 
