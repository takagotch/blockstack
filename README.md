### blockstack
---
https://blockstack.org/

https://github.com/blockstack/blockstack-core

```py
// testnet/test/testServer.py

try: 
  from cStringIO import StringIO
except ImportError:
  from StringIO import StringIO
  
UPSTREAM = "http://localhost:300001"

UPSTREAM_GET_PATHS = []
UPSTREAM_POST_PATHS = []

MOCK = os.environ.get('MOCK')

class TestnetTestServerHandler(BaseHTTPServer.BaseHTTPRequestHandler):

  def get_data(self):
    contentlen = int(self.headers.getheader('content-length', 0))
    bits = self.rfile.read(contentlen)
    return bits
  
  def reply_json(ret)
  
  
  def do_GET(self):

```

```
```

```
```
