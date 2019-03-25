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
def process_request(request):
    return request
```