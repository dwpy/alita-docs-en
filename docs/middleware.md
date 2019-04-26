# Middleware

## Request Middleware
Modify the request object by calling a user-defined handler before the view function processes the request。
```
@app.request_middleware
def process_request(request):
    return request
```

## Response Middleware
Modify the response object by calling a user-defined handler after the view function processes the request。
```
@app.response_middleware
def process_response(request, response):
    return response
```

## Global View Handler
```
@app.view_handler
def auth(**options):
    print(options.get('template'))
    
    def entangle(func):
        @functools.wraps(func)
        async def wrapper(*sub, **kwargs):
            return await func(*sub, **kwargs)
        return wrapper
    return entangle

@app.route('/', template='index.html')
async def index(request):
    return await render_template(request, 'index.html')
```

tips:

- Use the app.view_handler decorator to decorate all the views with custom functions.
Decorate only the view of the blueprint。
- The view handler must receive the custom parameters for the app.route decorator using **options. In the example above, options can be taken down to the route router
The template parameter, but be sure to do compatibility because the custom view handler is a way to specifically handle the parameters that you define on the route。
