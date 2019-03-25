# Static File
Dynamic web applications also require static files, usually CSS and JavaScript files。

## Create Static Folder
Create a folder called `static` in your package or module directory。

## Static Folder Configuration
The following code example is a blueprint for implementing a simple return text。
```
from alita import Alita

app = Alita('dw', static_folder='static', static_url_path='/static')
```
`static_folder` Point to the folder directory you created，`static_url_path`Represents the routing address where the application accesses a static file，
default is: '/static'。
