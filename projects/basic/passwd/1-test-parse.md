# Test Parse Valid /etc/passwd file

*Difficulty Level: Medium*

:star2: Open `passwd_test.go` and create a test function `TestParsePasswd`

```go
func TestParsePasswd(t *testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1. :star2: Copy the data from the [example_passwd](example_passwd) into a new variable `testData`.

1. :star2: Create a new io.Reader from the `testData` bytes (you can use `bytes.NewReader([]byte(testData))` and assign it to a variable.).

1. :star2: Call `passwd.ParseReader` (code is [here](https://github.com/willdonnelly/passwd/blob/master/passwd.go#L42-L57)) with the supplied bytes 
and verify no error is returned.  Assign the results to a variable `entries` map

1. :star2: Verify that the # of entries returned from `passwd.ParseReader` matches the # of lines in the `testData` variable (36 lines).

1. :star2: Verify that the entries map contains a value for the `ntp` username.  Verify the UID, GID, and other values match what should be expected. 

