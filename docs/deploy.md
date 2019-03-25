# Deploy

## Local Deploy
If you only want to deploy web applications locally, and currently `Alita` only supports single inheritance, you can create an app file like the following example code。
```
from alita import Alita

app = Alita('dw')


@app.route('/hello')
async def hello(request):
    return 'Hello, World!'


if __name__ == '__main__':
    app.run()
```

## Start Params
- host：server address
- port：server port
- debug：if debug mode

## user Gunicorn
`Gunicorn` is a unix-powered WSGI HTTP server. You need to specify the worker-class parameter to run the `Alita` application.。
```
gunicorn app:app -b 0.0.0.0:8000 -k alita.GunicornWorker
```
Abount `gunicorn`, please refer to the official documentation。
