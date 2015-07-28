## Make tests more readable

Since tests in Go are just Go code, you can define helper functions for making your Go tests more legible and making DRY (Don't Repeat Yourself) test code.

This was my rationale for the functions `initTestServer`, `makeWebSocketConn`, and `readMessagesAndKeepTheLastOne`, as well as using variations of the `expect` and `refute` helper functions in [the tests for Negroni](https://github.com/codegangsta/negroni/blob/master/negroni_test.go).

Making test code that's easy to read is especially important for writing Go packages because in Go, people who are still confused about how a function, data structure, or API is supposed to work often read the tests, which show examples with real Go code.

:star: Replace the calls to `ReadMessage` where it is expected that a `Conn` has no incoming messages with a helper function.

:star: While `expectF` and `refuteF` are good for giving Go code an `expect` syntax, on failing calls to those functions it can be hard to figure out the context of the failing call to `expectF` and `refuteF` since those functions make it so `t.Fatalf` is always called from the same line number.

Add in variations of these expect functions that allow you to pass in a context string for the expactations, like `expectFWithContext(other parameters..., "Expecting conn1 to not have any message to read")` or any other variation of an expect function you think would be useful.

:star: If there's anywhere else where you think a helper function would make the test code more readable, feel free to send in a pull request!