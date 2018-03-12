# sessions

Forked from [gin-contrib/sessions](https://github.com/gin-contrib/sessions) and simply replace [gopkg.in/mgo.v2](https://github.com/go-mgo/mgo/tree/v2) with [globalsign/mgo](https://github.com/globalsign/mgo)

# file tests
```
Running tool: /usr/local/Cellar/go/1.9.2/libexec/bin/go test -timeout 30s sessions -run ^TestMongo_SessionGetSet|TestMongo_SessionDeleteKey|TestMongo_SessionFlashes|TestMongo_SessionClear|TestMongo_SessionOptions$

ok  	sessions	0.042s
Success: Tests passed.
```