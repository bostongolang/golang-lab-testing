# Test Bad Config Returns Error 

*Difficulty Level: Easy*

:star2: Create a test function `TestBadConfigReturnsError`

```go
func TestBadConfigReturnsError(t *testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1.  :star2: Using the function `TestHostSection` as an example (code is [here](https://github.com/dullgiulio/sshconfig/blob/master/parse_test.go#L15-L48)),
create a test that uses a bad configuration by replacing `hostSection` with some malformed config, e.g.: 

```
# Some example Host section
NoHost asfsadf
blah 
fff  fff
```

1. :star2: Verify an error is returned on `sshconfig.Parse(reader(hostSection))`. 

