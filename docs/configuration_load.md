# Configuration Load

## Dict
```
app = Flask(__name__)
app.config['DEBUG'] = True
app.config.update(DEBUG=True)
```

## Module
```
import config
app.config_from_object(config)
```

## Python file
```
app.config_from_py('config.py')
```

## Json file
```
app.config_from_json('config.json')
```
