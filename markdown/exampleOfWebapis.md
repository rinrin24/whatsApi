# WebAPIの実用例

## 気象情報API
気象情報を取得できるAPIは多数公開されており、その利用例も多岐に渡っています。

[OpenWetherMap](https://openweathermap.org/)は、各地点の現在の天候、予報、履歴を取得できるAPIを提供しています。APIを利用するために取得する**APIキー**と、気象情報を取得したい都市の**都市ID**を指定してAPIにリクエストを送ることで、全世界各都市の気象情報を取得することができます。

潤沢な公開気象情報と強力な機械学習アルゴリズムを用いた気象予報の正確性などが高く評価されており、Google Maps JavaScript APIやUbuntu My Weather Indicatorなどの様々なサービスに利用されています。このほかにも多くの個人開発者によって利用されており、M5Stickの画面に傘の要不要を表示させる装置や、天候に応じたアドバイスをするLINEBotなどの作例が存在します。

<!-- 
resources:
https://github.com/chubin/wttr.in
https://openweathermap.org/
https://openweathermap.org/technology
https://openweathermap.org/examples
owmを使ってみる: 使い方の解説、実用例はなし
https://qiita.com/nownabe/items/aeac1ce0977be963a740
m5stickを玄関に取り付けて傘の要不要を報告させる
https://qiita.com/nih/items/5b122e9b43f3f10e7acf
m5stackの画面に天気を表示
https://qiita.com/kz1017/items/09a8c2aef2ece60a6128
-->

## 図書館API

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
