# RestAPI for Docker by Golang

## 思想
ネットに転がるものが`Gorilla mux`を用いたルーティングばかりなので標準ライブラリでHttpリクエスト毎にルーティングを行いたい

### 追記
Gorilla muxが便利すぎるので結局使うことにした

## 環境構築
```
$ docker-compose up --build -d
```

## 起動
```
$ docker exec -it docker_api_1 sh
$ go mod init
$ go mod tidy
$ go run main.go
```

## API確認

### HTTPリクエスト
```
GET http://localhost:7777/api/books
```

### 返却されるJSON
```
[
    {
        "id": "1",
        "title": "Book one"
    },
    {
        "id": "2",
        "title": "Book Two"
    }
]
```