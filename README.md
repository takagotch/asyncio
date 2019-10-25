### asyncio
---
https://github.com/python/cpython/tree/3.8/Lib/asyncio/

https://github.com/python/asyncio

https://docs.python.org/3/library/asyncio.html


```py
// cpython/Lib/asyncio/  
// sslproto.py

def _create_transport_context(sever_side, server_hostname):
  if server_side:
    raise ValueError('Server side SSL needs a valid SSLContext')

  sslcontext = ssl.create_default_context()
  if not server_hostname:
    sslcontext.check_hostname = False
  return sslcontext

_UNWRAPPED = "UNWRAPPED"
_DO_HANDSHAKE = "DO_HANDSHAKE"
_WRAPPED = "WRAPPED"
_SHUTDOWN = "SHUTDOWN"

class _SSLPile(object):

  max_size = 256 * 1024
  
  def __init__(self, context, server_side, server_hostname=None):

```

```
```

```
```


