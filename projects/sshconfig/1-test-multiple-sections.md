# Test Multiple Sections in SSH host config 

*Difficulty Level: Medium*

:star2: Create a test function `TestMultipleHostSections`

```go
func TestMultipleHostSections(t *testing.T) {
  //  TODO: YOUR TEST CODE HERE 
}
```

1.  :star2: Using the function `TestHostSection` as an example (code is [here](https://github.com/dullgiulio/sshconfig/blob/master/parse_test.go#L15-L48)),
create a test that has multiple Host Sections.  Replace the `hostSection` text with a test that has multiple host sections, e.g.:

```
# Some example Host section
Host local # Local SSH
  OptionOne do anything here
  OptionTwo 12345 # There is also a comment
  OptionWithoutValue
  OptionsWithComment # Comment
  
Host bob.example.com
  SendEnv DUO_PASSCODE
  ForwardAgent yes
```

1. :star2: Verify that the number of sections returned are 2.

1. :star2: Verify that the `Name` value of the second section is `bob.example.com`.

1. :star2: Verify there are 2 options returned and they match the `SendEnv` and `ForwardAgent` parameters. 


