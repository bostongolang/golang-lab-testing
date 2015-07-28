## A general overview of the structure of the web app

The structure of the web app is very similar to the [chat server in the concurrency lab](https://github.com/bostongolang/golang-lab-chat), but instead of the broadcaster broadcasting chat messages, it broadcasts locations, and instead of using TCP connections from the `net` package, it uses Gorilla Websocket connections.

## The app's front end

The web app's front-end is a Google Map where the user is able to use the W, A, S, and D keys to control their marker on the map (the hibiscus flower). When the user moves on the map, their location is send to the server and broadcasted to all other connected users so their marker's position is updated on all maps.

![Slothful Soda Tracker demo GIF](https://github.com/AndyHaskell/slothful-soda-tracker/blob/master/public/images/slothful-soda-tracker-demo.gif?raw=true)

## The major data types used on the server side

### `Broadcaster`

* A central data structure that allows users to communicate
* Gets notified any time a user joins, disconnects, or updates their location and broadcasts that information to all connected users.
* Made as an `interface` for testability

### `User`

* A structure that serves as a middleman between the client and the server.
* Has a `websocket.Conn` receiving messages from the client and a `chan []byte` receiving messages from the Broadcaster.
* Sends messages it receives on its `Conn` to the Broadcaster and sends messages it receives from the Broadcaster to the client on its `Conn`

### `websocket.Conn`

* A WebSocket connection from the client (the browser) and the server, made with the Gorilla Websocket package
* Messages between the client and the server are sent as JSON.

### `Msg`

* A generalized data structure to be converted to a JSON message containing a message type plus any other data that can be converted to JSON.
* Used for similar functionality to events in [the socket.io version of this web app](https://github.com/AndyHaskell/slothful-soda-tracker).

## The structure of the tests in `connect_test.go`

* The major testing packages used are:
  * `net/http/httptest` for the HTTP servers used in the tests
  * and `gorilla/websocket`, which is both used for making client-side connections to the web app in tests.
  * Gorilla Websocket connections and net/http requests are used for testing connections and WebSocket functionality from the client-side without the use of a browser.
    * The client-side WebSocket connections receive messages from a corresponding `Conn` on the server-side; any time a message is written from the server-side `Conn`, it can be read by the client-side `Conn` and vice versa.

* Helper functions are used in the tests to make the code readable.
  * `expectF` and `refuteF` are variations of the `expect` and `refute` functions used for testing Negroni.
  * `makeWebSocketConn` is used for dialing the WebSocket connection to make a client-side WebSocket connection.
  * `readMessagesAndKeepTheLastOne` takes in a client-side WebSocket connection and how many messages to read and does exactly what it says on the tin.