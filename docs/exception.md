# Exception
The `alita.exceptions` module defines the types of request codes for Http requests. You can also define exceptions of your own.
If it is not inherited from HTTPException, it is treated as a 500 exception。

## Exception Handle
You can use the `abort` function to automatically throw an exception that specifies the request code。
```
from alita.exceptions import abort

@app.route('/')
async def hello(request):
    abort(403)
```

You can also register custom handlers only if the system encounters an exception to this request error code or to this request class。
from alita.exceptions import NotFound

@app.register_error_handler(NotFound)
async def hello(request):
     return '404 error!'

@app.register_error_handler(404)
async def hello1(request):
     return '404 error!'
```

## Common Exception
- NotFound: view not found
- ServerError: internal serve error