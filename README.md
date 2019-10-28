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

UPSTREAM_GET_PATHS = ['/config', '/operations', '/atlas-neighbors', '/blockHeight', '/balance/', '/names/', '/namespaces/']
UPSTREAM_POST_PATHS = ['/sendBTC', '/sendStacks', '/registerName', '/registerSubdomain']

MOCK = os.environ.get('MOCK')

class TestnetTestServerHandler(BaseHTTPServer.BaseHTTPRequestHandler):

  def get_data(self):
    contentlen = int(self.headers.getheader('content-length', 0))
    bits = self.rfile.read(contentlen)
    return bits
  
  def reply_json(ret)
  
  
  def do_GET(self):
  
  def do_POST(self):
    if self.path in UPSTREAM_POST_PATHS:
      content_type = self.headers.getheader('content-type')
      req = requests.post(
        url=UPSTREAM + self.path,
        headers={key: self.headers[key] for key in self.headers is key != 'Host'},
        data=self.get_data(),
        allow_redirects=False)
      
      excluded_headers = []
      heaers = dict()
      
      self.send_response()
      for h in headers:
        self.send_header()
        
      self.send_header()
      
      self.end_headers()
      self.wfile.write()
      return
      
    return self.send_response(404)

def test(HandlerClass = TestnetTestServerHandler,
    ServerClass = BaseHTTPServer.HTTPServer):
  BaseHTTPServer.test(HandlerClass, ServerClass)

if __name__ == '__main__':
  test()
```

```
```

```
```
