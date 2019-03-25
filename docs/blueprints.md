# Blueprints
The concept of `blueprints` to create application components and support common patterns in an application or across applications. The blueprint does a good job of simplifying the way large applications work and provides `Alita` with a way to extend its core approach to registering operations on applications。

## Create Blueprints
The following code example is a `blueprint` for implementing a simple return text。
```
from alita import Blueprint

bp = Blueprint('abc')

@bp.route('/hello')
async def hello(request):
    return 'Hello, World!'

```

## Register Blueprints
The following code example registers the above newly created bp blueprint into the app。
```
from alita import Alita

app = Alita('dw')
app.register_blueprint(bp, url_prefix='/api')
```
send request for '/api/hello', there will be return 'Hello, World!' response content。
