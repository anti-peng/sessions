# sessions

Forked from [gin-contrib/sessions](https://github.com/gin-contrib/sessions) and simply replace [gopkg.in/mgo.v2](https://github.com/go-mgo/mgo/tree/v2) with [globalsign/mgo](https://github.com/globalsign/mgo)

# file tests
```
Running tool: /usr/local/bin/go test -v -timeout 30s sessions -run ^TestMongo_SessionGetSet|TestMongo_SessionDeleteKey|TestMongo_SessionFlashes|TestMongo_SessionClear|TestMongo_SessionOptions$

=== RUN   TestMongo_SessionGetSet
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /set                      --> sessions.sessionGetSet.func1 (4 handlers)
[GIN-debug] GET    /get                      --> sessions.sessionGetSet.func2 (4 handlers)
[GIN] 2018/03/13 - 16:37:32 | 200 |     944.481µs |                 | GET      /set
[GIN] 2018/03/13 - 16:37:32 | 200 |     654.331µs |                 | GET      /get
--- PASS: TestMongo_SessionGetSet (0.01s)
=== RUN   TestMongo_SessionDeleteKey
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /set                      --> sessions.sessionDeleteKey.func1 (4 handlers)
[GIN-debug] GET    /delete                   --> sessions.sessionDeleteKey.func2 (4 handlers)
[GIN-debug] GET    /get                      --> sessions.sessionDeleteKey.func3 (4 handlers)
[GIN] 2018/03/13 - 16:37:32 | 200 |     529.402µs |                 | GET      /set
[GIN] 2018/03/13 - 16:37:32 | 200 |     988.828µs |                 | GET      /delete
[GIN] 2018/03/13 - 16:37:32 | 200 |      363.64µs |                 | GET      /get
--- PASS: TestMongo_SessionDeleteKey (0.00s)
=== RUN   TestMongo_SessionFlashes
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /set                      --> sessions.sessionFlashes.func1 (4 handlers)
[GIN-debug] GET    /flash                    --> sessions.sessionFlashes.func2 (4 handlers)
[GIN-debug] GET    /check                    --> sessions.sessionFlashes.func3 (4 handlers)
[GIN] 2018/03/13 - 16:37:32 | 200 |      556.48µs |                 | GET      /set
[GIN] 2018/03/13 - 16:37:32 | 200 |    1.055132ms |                 | GET      /flash
[GIN] 2018/03/13 - 16:37:32 | 200 |     862.788µs |                 | GET      /check
--- PASS: TestMongo_SessionFlashes (0.01s)
=== RUN   TestMongo_SessionClear
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /set                      --> sessions.sessionClear.func1 (4 handlers)
[GIN-debug] GET    /check                    --> sessions.sessionClear.func2 (4 handlers)
[GIN] 2018/03/13 - 16:37:32 | 200 |     669.171µs |                 | GET      /set
[GIN] 2018/03/13 - 16:37:32 | 200 |     403.798µs |                 | GET      /check
--- PASS: TestMongo_SessionClear (0.00s)
=== RUN   TestMongo_SessionOptions
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /domain                   --> sessions.sessionOptions.func1 (4 handlers)
[GIN-debug] GET    /path                     --> sessions.sessionOptions.func2 (4 handlers)
[GIN] 2018/03/13 - 16:37:32 | 200 |     522.113µs |                 | GET      /domain
[GIN] 2018/03/13 - 16:37:32 | 200 |     495.957µs |                 | GET      /path
--- PASS: TestMongo_SessionOptions (0.00s)
PASS
ok  	sessions	0.047s
Success: Tests passed.
```