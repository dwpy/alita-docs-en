# Route

## Defile Route
Using the `route()` decorator, you can bind a function to a URL。
```
@app.route('/hello')
def hello(request):
    return 'Hello World'
```
You can also add view functions using the `add_url_rule()` method, for example：
```
def hello(request):
    return 'Hello World'
app.add_url_rule(hello, '/hello')
```

## Route Params
Custom variables can be added to the routing address and passed to the view function. `str`, `int`, `float` and `path` are supported.
If the variable name is not defined in the view parameter, an error is reported when the interface is invoked, as shown below：
```
@app.route('/user/<name:str>')
def hello(request, name):
    return 'Hello World, %s' % name
```
Note: if written `<name>` , the default is `str`。

## Route Function Params
- methods: View functions are requested by default 'GET'。
- endpoint: Map endpoint between view function and routing rule. User can customize this value. Default is name of view function。