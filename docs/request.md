# Request

## Request Data
When the client calls the server interface, it creates the `request` object, which contains the following data, and passes it to the view function：

- json(dict)：request body json data。
- args(dict)：URL request params。
- body(bytes)：The original request body。
- headers(dict)：request headers。
- cookies(dict)：request cookies。
- method(str)：request method。
- host(str)：request host address。
- port(int)：request port。
- path(str)：request path。
- app(object)：server app object。
- query_string(str)：request query string。