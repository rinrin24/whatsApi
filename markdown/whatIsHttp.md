# HTTPとは？
インターネット上で情報の送受信を行う際には、**HTTP**(**H**yper**t**ext **T**ransfer **P**rotocol)と呼ばれる約束事に従って通信が行われます。ここでは、Webブラウザで`https://developer.mozilla.org/index.html`を表示する場合を例に、HTTPによる通信の流れを追ってみましょう。

HTTPの通信は**クライアント**と**サーバー**の間で行われます。クライアントは、サーバー上にある文書や画像といったリソースの送信や、サーバー上の情報の変更などをサーバーに要求します。今回の例では、Webブラウザはサーバー上のファイル`index.html`を要求しており、クライアントに該当します。一方、サーバーはクライアントの要求に応えてリソースを返したり、サーバー上の情報を変更したりします。今回はWebブラウザからの要求を受け取って`index.html`を返すWebサーバーがサーバーに該当します。

## リクエスト
クライアントがサーバーに送るリソース送信や情報更新などの要求を、**リクエスト**と呼びます。以下は`developer.mozilla.org/index.html`の送信を要求するリクエストの例であり、Webブラウザがこのページの閲覧を試みる際にWebサーバーに送信されます。

```HTTP
GET /index.html HTTP1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
```

HTTPのリクエストは、大きく分けて**メソッド**と**ヘッダ**の2つの要素によって構成されています。

### メソッド
メソッドはリクエストの1行目に書かれており、クライアントが実行したい操作を指定します。今回の例ではサーバーからリソースを取得したいので、`GET`メソッドを使用しています。同じ1行目にはこのほかに、サーバー内でリソースが存在する場所を示す**パス**と、HTTPプロトコルのバージョンが記されています。

今回の例のように、`GET`メソッドはサーバーからリソースを取得したいときに使用します。HTTPの仕様上、`GET`メソッドはサーバーの状態を変化させないメソッドであり、サーバーからの情報取得のみを行うリクエストに使用されることが望ましいメソッドです。

`POST`メソッドはサーバーにデータを送信する際に使用します。`POST`メソッドを使用するリクエストでは、サーバーに送信するデータを**ボディ**として付加したリクエストが送信され、その内容に従ってデータ更新などの処理がサーバー上で行われます。

### ヘッダ
ヘッダには、サーバーに渡す追加情報をリクエストに付加する役割があります。今回の例では、2行目の`Host`ヘッダにリクエストが送信される先のサーバーのホスト名が、3行目の`User-Agent`ヘッダにクライアントの情報がそれぞれ指定されています。

## レスポンス
クライアントからのリクエストを受け取ったサーバーは、これに対する返答、すなわち**レスポンス**を返します。以下は`developer.mozilla.org/index.html`へのリクエストに対するレスポンスの例です。

```HTTP
HTTP/1.1 200 OK
Date: Sat, 09 Oct 2010 14:28:02 GMT
Server: Apache
Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
ETag: "51142bc1-7449-479b075b2891b"
Accept-Ranges: bytes
Content-Length: 29769
Content-Type: text/html

<!DOCTYPE html...（ここに、リクエストした 29769 バイトのウェブページが来ます）
```

1行目にはHTTPプロトコルのバージョン、さらにレスポンスの性質を示す数字とそれに対応するキーワードの組である**ステータスコード**が示されています。

2行目から始まる要素は**ヘッダ**であり、リクエストヘッダと同様にクライアントへ渡す追加情報が付加されています。

ヘッダの末尾には空行が置かれ、その次の行から要求されたリソースそのものである**ボディ**が始まっています。

## まとめ
HTTPによる通信では、初めにWebブラウザなどのクライアントから**リクエスト**が行われます。リクエストを受け取ったサーバーは返答として**レスポンス**を返します。

## 参考文献
- [HTTPの概要 | MDN Web Docs](https://developer.mozilla.org/ja/docs/Web/HTTP/Overview) (2023/11/20 閲覧)
- [GET - HTTP | MDN Web Docs](https://developer.mozilla.org/ja/docs/Web/HTTP/Methods/GET) (2023/11/20 閲覧)
- [POST - HTTP | MDN Web Docs](https://developer.mozilla.org/ja/docs/Web/HTTP/Methods/POST) (2023/11/20 閲覧)
- [Safe (安全) (HTTP メソッド) | MDN Web Docs](https://developer.mozilla.org/ja/docs/Glossary/Safe/HTTP)
- [Idempotent (べき等) | MDN Web Docs](https://developer.mozilla.org/ja/docs/Glossary/Idempotent)
