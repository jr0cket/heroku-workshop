# Common error messages 

  Whenever your app experiences an error Heroku returns a standard error page with HTTP status code `503`. To debug the underlying error Heroku also adds custom error information to your log entries. Each type of error gets its own error code, with all HTTP errors starting with the letter `H` and all runtime errors starting with `R`. Logging errors start with `L`.

## Heroku Error codes

| Code | Name | Description |
| -- | -- | -- |
| `H12` | Request timeout | An HTTP request took longer than 30 seconds to complete causing a [request timeout](https://devcenter.heroku.com/articles/request-timeout)
| `H14` | No web dynos running | check your app in the resouces tab of the dashboard or with `heroku ps`
| `H18` | Request Interrupted | Either the client socket or your web process socket was closed before the backend returned an HTTP response
| `H19` | Backend connection timeout | routing could not connect to your web process within 5 seconds, a sign your app is overwhelmed
| `H20` | App boot timeout | At least 1 web dyno must reach the “up” state within 75 seconds or the router logs an `H20` error & serves a standard error page
| `H80` | Maintenance mode | see guide to [maintenance mode](https://devcenter.heroku.com/articles/maintenance-mode), if certain you can swich maintenance mode off with `heroku maintenance:off`
| `R12` | Exit timeout |  process failed to exit within 10 seconds of being sent a SIGTERM, so the process is sent SIGKILL to force an exit
| `R99` | Platform error | check [Heroku Status](https://status.heroku.com) for details if you see these error codes

> **Info** See the full list of [Heroku error codes](https://devcenter.heroku.com/articles/error-codes) for more details.

## Http Status codes

  There are well defined error codes when communicating via HTTP/S.  Its useful to know a few of the key codes so you can understand the log output quicker should their be an issue.

  * `200 OK` - Standard response for successful HTTP requests. 
  * `400 Bad Request` - server cannot or will not process the request due to a client error.
  * `403 Forbidden` - a valid request, but the server is refusing to respond, authenticating makes no difference.
  * `404 Not Found` - requested resource could not be found
  * `408 Request Timeout` - server timed out waiting for the request.
  * `500 Internal Server Error` - an unexpected condition was encountered and no more specific message is suitable.
  * `503 Service Unavailable` - server is currently unavailable, eg. its overloaded or down for maintenance.

> **Info** For more details on HTTP errors, see the [List of HTTP status codes](http://en.wikipedia.org/wiki/List_of_HTTP_status_codes) on Wikipedia.
