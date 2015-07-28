## go-slothful-soda-tracker

The Slothful Soda Tracker is a WebSocket-based web app made by sloths living at the Fresh Pond in Cambridge. The sloths there invented a hibiscus-flavored soda, called Slothful Soda, which they deliver to Ultimate Frisbee players across the Boston area using quadcopters. Because it's such a popular soda, the sloths made a WebSocket-based delivery tracker web app showing the locations of all of the delivery quadcopters.

The structure of the web app is very similar to the [chat server in the concurrency lab](https://github.com/bostongolang/golang-lab-chat), but instead of the broadcaster broadcasting chat messages, it broadcasts locations, and instead of using TCP connections from the `net` package, it uses Gorilla Websocket connections.

## Step 1: Project Setup

1. :star2: Fork the Github project [https://github.com/AndyHaskell/go-slothful-soda-tracker](https://github.com/AndyHaskell/go-slothful-soda-tracker).

   * :question: If you need help, please see [this document](https://help.github.com/articles/fork-a-repo/) or ask a TA for help.

2. :star2: Clone your fork of your repo to your $GOPATH source path 

```
cd $GOPATH/src 
mkdir -p github.com/<youraccount>
cd github.com/<youraccount>
git clone git@github.com:<youraccount>/go-slothful-soda-tracker.git
cd go-slothful-soda-tracker
```

3. :star2: Run `go test -v .` to ensure that the existing tests run.
   * :question: If you need help getting the project tests to run, ask your TA.

4. Optionally, run `go install` and `go-slothful-soda-tracker` and go to `localhost:1123` in a few browser windows to try out the web app for yourself!
