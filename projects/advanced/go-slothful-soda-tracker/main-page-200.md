## Testing an HTTP connection to the main page

To test an HTTP connection to the main page, we can use the `net/http/httptest` library.

* httptest comes with its own `Server` type made for testing. You can create one by passing in a `Handler` such as a `ServeMux`. For example:

```go
testSvr := httptest.NewServer(http.HandlerFunc(func(w http.ResponseWriter, r *http.Request)){
    fmt.Fprintf(w, "This is a test server with a simple HandlerFunc as its Handler")
})
```

* You can then use `net/http`'s functions like `http.Get` to send requests to the server's URL (httptest servers generate their own URLs) and see what the response is.

```go
res, err := http.Get(testSvr.URL)
```

* The Slothful Soda delivery tracker creates its `ServeMux` by passing a `Broadcaster` interface into its own `initMux` function. When we don't need the actual `Broadcaster` functionalty, we can pass in a `*EmptyBroadcaster` to `initMux.`

:star: Create a test function `TestMainPage200` that makes sure we get a 200 if we send an HTTP request to the `/` route on the server's `ServeMux`.