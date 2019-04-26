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
- rule: View function route rule。
- methods: View functions are requested by default 'GET'。
- endpoint: Map endpoint between view function and routing rule. User can customize this value. Default is name of view function。
- options: Variable parameters, user-defined function parameters, mainly for global view processing functions。

## `url_for` Function
Both the App object and blueprint object can use the url_for function to generate the view URL by specifying the endpoint。

Used in view functions:
```
@app.route('/')
async def index(request):
    url = app.url_for('index1')
    return RedirectResponse(url)
```

Used in blueprint functions:
```
br = Blueprint('demo')

@br.route('/')
async def index(request):
    url = app.url_for('index1')
    return RedirectResponse(url)
```

Used in template:
```
<h1><a href="{{url_for('index1')}}">test</a></h1>
```
