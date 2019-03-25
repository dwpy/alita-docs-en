# First Application

## Runtime Environment
> Python3.5+


## Install
> python3 -m pip install alita

## Example
```
from alita import Alita
app = Alita()

@app.route('/')
async def hello(request):
    return 'Hello World!'

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=8000)
```

start server: `python3 main.py` \
open this address: `http://0.0.0.0:8000`，then you will see: *Hello World!*。

