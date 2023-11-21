# WebAPIの実用例

## 気象情報API
気象情報を取得できるAPIは多数公開されており、その利用例も多岐に渡っています。

[OpenWetherMap](https://openweathermap.org/)は、各地点の現在の天候、予報、履歴を取得できるAPIを提供しています。APIを利用するために取得する**APIキー**と、気象情報を取得したい都市の**都市ID**を指定してAPIにリクエストを送ることで、全世界各都市の気象情報を取得することができます。

潤沢な公開気象情報と強力な機械学習アルゴリズムを用いた気象予報の正確性などが高く評価されており、Google Maps JavaScript APIやUbuntu My Weather Indicatorなどの様々なサービスに利用されています。このほかにも多くの個人開発者によって利用されており、M5Stickの画面に傘の要不要を表示させる装置や、天候に応じたアドバイスをするLINEBotなどの作例が存在します。

## カーリル図書館API
全国の図書館資料の横断検索を行うことができるサービス「カーリル」は、その蔵書検索機能をWebAPIとして提供しています。

カーリルでは、各図書館が導入している複数の蔵書管理システムに対応するために、各蔵書検索システムに**システムID**が割り振られており、これを用いて自治体ごとの蔵書の情報を取得することができます。

さらに、世界中で発行される書籍には、1書名ごとに**ISBN**と呼ばれる13桁の一意な番号が割り振られており、カーリルの図書館APIではこれを用いて書籍情報を取得することができます。

図書館APIが公開された2010年、図書館APIを利用した作品を公募する「カーリルAPIコンテスト」が実施されました。グランプリには、Twitter上で「@calilun「○○県△△市」で「著書名」借りられる？」とリプライすると貸出可能かどうか答えるTwitterBot「かーりるん」が選出されました。

図書館APIはこのほかにも、都道府県別に著書の所蔵状況を表示した地図や、Amazonの書籍購入ページ上に近隣図書館での所蔵状況を表示するGoogle Chrome拡張機能などにも利用されています。

<!-- 
resources:
https://api.calil.jp/check?appkey=insert-your-app-key&isbn=4150115311&systemid=Tokyo_Toshima
豊島区内でのグレッグ・イーガン『ディアスポラ』(ハヤカワ文庫SF、2005)の所蔵状況

https://twitter.com/kurubushi_rm/status/1348217400626302977
『独学大全』著者による都道府県別の所蔵状況マップ

https://sonohon.com/
Amazonの書籍購入ページ上に近隣図書館での所蔵状況を表示するGoogle Chrome拡張機能
-->

## Random Dog API
Random Dog APIは、犬の画像や動画をランダムに取得できるAPIを提供しています。リクエストに付加する引数によって、画像および動画のファイル形式を絞り込んで取得することができるようになっています。

以降の章で、HTTP通信を介したWebAPIの利用を、実際にこのAPIを用いて試してみましょう。

<!-- 
resources:
https://random.dog/
 -->

## 参考文献
### 気象情報API
- [OpenWeatherMap](https://openweathermap.org/) (2023/11/21 閲覧)
- [Weather model | OpenWeatherMap](https://openweathermap.org/technology)
- [Partners and Solutions | OpenWeatherMap](https://openweathermap.org/technology)
- [【M5Stick】天気予報が雨の時、傘を持つように促す装置を作った[天気の戸締まり] by @nih | Qiita](https://qiita.com/nih/items/5b122e9b43f3f10e7acf)
- [毎日のお天気と雨の日の準備を朝にLINEに送ってくれるBot by @rechiba3 | Qiita](https://qiita.com/rechiba3/items/faa2e79c725266584de2)

### カーリル図書館API
- [図書館API | カーリル](http://calil.jp/doc/api.html)
- [カーリルAPIコンテスト　結果発表！ | カーリルのブログ](https://blog.calil.jp/2010/05/api_01.html)
- [Xユーザーの読書猿『独学大全』14刷26万部、『文章大全』執筆中さん: 「県立レベルの図書館で『独学大全』を所蔵していただいている都道府県 カーリルAPI &amp; Google Chart APIを使いました。関東〜甲信越が空白になってますが、市町村立図書館では所蔵していただいてます。」 / X](https://t.co/5QjAfCCvdT)
- [その本、図書館にあります。](https://sonohon.com/)

### Random Dog API
- [random.dog](https://random.dog/)
- [adenflorian/random.dog: woof | GitHub](https://github.com/AdenFlorian/random.dog)
