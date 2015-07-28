# Create URL shortener tests 

*Difficulty Level: Advanced*

The goal is to write at minimum 2 tests: one that tests the output of a POST to generate a shortened URL, and one that verifies that the valid shortened URL redirect is returned.

Note - these tests will have less guidance than the `basic` tests.  You may also have to refactor some of the original project code
to make it more testable.  Here are some ideas on how to setup tests for the project.

1. :star2: Currently, the `short.go` server code [requires a redis server connection](https://github.com/johnnye/short/blob/master/short.go#L36-L46). How can you 
set up your tests to work? Some ideas:
   
  * Refactor the code so that you can supply a mock 'redis' server
  * Require a redis localhost connection to run the tests, and create a setup function you run [TestMain](http://golang.org/pkg/testing/) that will clear the redis database
    and prepare for a test connection.

1. :star2: Since this is a webserver, you will need to think about what strategy you are going to test the POST and GET handlers.  To do a full integration test, you can start up the webserver in `TestMain`.  Or, you can build mocks for each handler as described in this [document](http://www.markjberger.com/testing-web-apps-in-golang/).

1. :star2: Write a test that verifies the POST to / correctly returns a shortened URL for the URL http://example.com (see the curl command in the README for an example of the JSON
parameters expected).  

1. :star2: Write a test that verifies GETing a shortened URL returns a HTTP redirect to the correct website.  E.g., if the POST request above returns http://127.0.0.1/ABC, running GET http://127.0.0.1/ABC should redirect me to http://example.com.
