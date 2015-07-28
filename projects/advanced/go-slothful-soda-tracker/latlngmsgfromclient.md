## Test `latLngMsgFromClient`

Last night I added `latLngMsgFromClient` so that the JSON messages sent from the browser to a `User`'s `Conn` only contain a pair of latitude and longitude coordinates. In `latLngMsgFromClient`, these coordinates are converted to a `LatLngMsg` struct that has both the coordinates and the `User`'s ID string, which are then sent to the `Broadcaster` as JSON.

Before I added `latLngMsgFromClient`, the user's coordinates and ID number were sent from the browser, which turned out to create a security hole where a user could move any other user's location since the JSON being sent from the browser included an ID number.

:star: In `connect_test.go`, add a function `TestLatLngMsgWithWrongId` that connects two users to a test server, sends the JSON of a valid pair of latitude and longitude coordinates but the wrong ID number (for example, have the first connection send `{"id":"2","lat":42.4069,"lng":-71.1198}`) and makes sure a JSON message with the correct ID number is sent (`{"id":"1","lat":42.4069,"lng":-71.1198}`).

:star: In `connect_test.go`, add a function `TestLatLngMsgWithInvalidJSON` to make sure a coordinate message with invalid JSON like `(42.4069,-71.1198)` does not reach the `Broadcaster`.

:star: Since the `User` data structure functions as a middleman between the client-side `Conn`s and the `Broadcaster`, right now it's hard to test the `User`'s methods like `latLngMsgFromClient` by itself. Refactor the code so that converting the original JSON coordinates to a JSON encoding of a `LatLngMsg` is separate from receiving the message on the `User`'s server-side `Conn`.