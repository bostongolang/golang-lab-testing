# Test bad CSV file returns an error 

*Difficulty Level: Medium*

:star2: Open `parse_test.go`. Create a function `TestBadCSVReturnsError` 

```go
func TestBadCSVReturnsError(t *testing.T){

  // TODO test code here

}
```

The goal of this task is to modify [LoadFile](https://github.com/mabetle/gocsv/blob/master/parser.go#L22-L51) so that it returns an error on a bad CSV parse, then
write a test that attempts to parse some bad CSV file.

1. :star2: In `parser.go`, modify `LoadFile`'s signature so it returns `(*CSV, error)`, then modify all of the places were it prints an error to return `nil, error` instead.  

   :star2: Adjust all calls to `LoadFile` within the project to reflect this new function signature.

1. :star2: Create some test data `bad_data.csv` and fill out the code in `TestBadCSVReturnsError` to verify that `nil, error` is returned from `LoadFile` when parsing this data.
