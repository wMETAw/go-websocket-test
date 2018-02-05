# WebSocket
https://echo.labstack.com/cookbook/websocket


## Usage

```
# Install dep (for the first time only)
$ go get -u github.com/golang/dep/cmd/dep

# lunch net or gollira package
$ go run net/server.go
or
$ go run gollira/server_gollira.go


$ open public/index.html
```


## Debug

```
curl -v -i -N \
  -H 'Sec-WebSocket-Version: 13' \
  -H "Sec-WebSocket-Key: $(head -c 16 /dev/urandom | base64)" \
  -H "Connection: Upgrade" \
  -H "Upgrade: websocket" \
  "http://localhost:1323/ws"
```

## dep Usage

```
# 最初の一回のみ行います。現在の構成を解析し`Gopkg.toml`、`Gopkg.lock`が生成されます。
dep init

# パッケージをvendorディレクトリ以下にインストールします
dep ensure

# 新しいパッケージを依存関係に追加しインストールを行う
dep ensure -add github.com/foo/bar

# パッケージをアップデートする
dep ensure -update github.com/foo/bar

# 現在の状態を出力する
dep status
```