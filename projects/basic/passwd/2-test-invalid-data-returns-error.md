# Test Parse Invalid Data Returns Error 

*Difficulty Level: Easy*

:star2: Open `passwd_test.go` and create a test function `TestInvalidPasswdReturnsError`

```go
func TestInvalidPasswdReturnsError(t *testing.T) {
  //  TODO: YOUR TEST CODE HERE 

}
```

1. :star2: Create a variable `testData` that has an invalid passwd file.

```
testData := `root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
some invalid data
`
```

1. :star2: Create a new io.Reader from the `testData` bytes (you can use `bytes.NewReader([]byte(testData))` and assign it to a variable.).

1. :star2: Call `passwd.ParseReader` (code is [here](https://github.com/willdonnelly/passwd/blob/master/passwd.go#L42-L57)) with the supplied bytes.

1. :star2: Verify that an error is returned.

