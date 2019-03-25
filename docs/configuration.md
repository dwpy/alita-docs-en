# Config

## DEBUG

- default：`False`

If `DEBUG` mode is turned on, detailed errors can be seen after it is turned on. `Autoreload` can be achieved without restart after code modification。

## SECRET_KEY

- default：`None`

The secret key, If `SESSION_USE_SIGNER` is True, then use it。

## MAX_CONTENT_LENGTH

- default：`None`

If set to the number of bytes, `Alita` will refuse content length request into greater than this value, and return a status code of 413。


## SEND_FILE_MAX_AGE

- default：`12 * 60 * 60`

The maximum duration of the default cache control, in seconds。


## SESSION_COOKIE_NAME

- default：`sessionid`

The name of the session cookie。

## SESSION_COOKIE_EXPIRE

- default：`None`

The expire time of the session cookie。

## SESSION_COOKIE_DOMAIN

- default：`None`

The domain of the session cookie。

## SESSION_COOKIE_PATH

- default：`None`

The path of the session cookie。

## SESSION_COOKIE_HTTPONLY

- default：`True`

Controls whether cookies should be set to `httponly` flags。

## SESSION_COOKIE_SECURE

- default：`False`

Controls whether cookies should be set with security flags。

## SESSION_COOKIE_SAMESITE

- default：`None`

Control cookie cross - site request forgery。

## SESSION_KEY_PREFIX

- default：``

session_key prefix。

## SESSION_USE_SIGNER

- default：`False`

Whether `sessionid` needs to be signed, work with `SECRET_KEY`。

## SESSION_SAVE_EVERY_REQUEST

- default：`False`

Controls whether `session` need to be saved on every request。


## SESSION_EXPIRE_AT_BROWSER_CLOSE

- default：`False`

Controls whether the `session` expires after the page is closed。

## SESSION_TABLE_NAME

- default：`session`

session save table name。

## SESSION_ENGINE

- default：`None`

`session` manage component。

## SESSION_ENGINE_CONFIG

- default：`None`

`session`  manage component database configuration。

