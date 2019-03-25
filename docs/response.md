# Response

## Text
```
from alita.response import TextResponse
@app.route('/')
async def hello(request):
    return TextResponse('Hello World!')
```

## Html
```
from alita.response import HtmlResponse
@app.route('/')
async def hello(request):
    return HtmlResponse('Hello World!')
```

## Dict
```
from alita.response import JsonResponse
@app.route('/')
async def hello(request):
    return JsonResponse('Hello World!')
```

## File
```
from alita.response import FileResponse
@app.route('/')
async def hello(request):
    return FileResponse('static/test.txt')
```

## Redirect
```
from alita.response import RedirectResponse
@app.route('/')
async def hello(request):
    return RedirectResponse('/user')
```
Note: if no specific response class is specified, it is automatically matched based on the type returned, using `TestResponse` if a string, or `JsonResponse` objects if a dictionary or list。
