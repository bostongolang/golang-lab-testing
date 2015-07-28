# Refactor the directory listing code

*Difficulty Level: Advanced*

The goal of this task is to refactor the directory parsing and formatting code to make it more testable.  

1. :star2: In `koala.go`, create two functions that encapsulate selected code from the main function.  The 

```
//
// getFiles should take an input path and walk the directory from the `rootDir`
//
func getFiles(rootDir string) (files []string, err error) {
    // refactored from the code here: https://github.com/gokyle/koala/blob/master/koala.go#L68-L105
}

//
// formatFiles() will output 
//
func formatFiles(files []string, style string) string {
  // refactored from here: https://github.com/gokyle/koala/blob/master/koala.go#L107-L108
  
}
```


1. :star2: Replace the code in the `main()` function with calls to getFiles() and formatFiles().  Make sure the output of the command line tool does not change. 

1. :star2: In `koala_test.go`, write a test for `getFiles()` (you can use a temporary directory to set up the expected file struction).

1. :star2: In `koala_test.go`, write tests for `formatFiles()` for every expected format (lisp, space, comma, null) given an array of file strings.

