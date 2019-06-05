# WebSocket
WebSocket is a protocol that HTML5 began to provide for full duplex communication over a single TCP connection.

## view
```
@app.websocket('/ws')
async def websocket_view(ws, request):
    message = await ws.recv()
    await ws.send(message)
```

## blueprint view
```
from alita import Blueprint

bp = Blueprint('abc')

@bp.websocket('/ws')
async def websocket_view(ws, request):
    message = await ws.recv()
    await ws.send(message)
```
