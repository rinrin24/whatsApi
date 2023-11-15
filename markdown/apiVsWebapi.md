# APIとwebAPIの違いって？

## Webapiとapiについて

## RESTapi、SOAP、xml over http、json over httpの違い
### 1.RESTapi
RESTapiは、*Representational State Transfer*の略です。
ロイ・フィールディングの論文%*1%{#ff0000}を元にした、6つの項目をすべて満たす通信インターフェイスを設計するためのアーキテクチャスタイルの事を言います。（以下は論文中に記されている6項目）
- *ClientServer*（送信者と受信者の独立）
- *Stateless*（以前のリクエストとは関係なく、新しいリクエストを処理する）
- *Cache*（全ての API レスポンスはキャッシュ可能である）
- *Uniform Interface*（統一された標準形式でデータを返す）
- *Layered System*（階層システム）
- *Code-On-Demand*（API レスポンスに、必要に応じてコードスニペットを含めることができる。）

#### 1.a RESTのメリット
REST はメッセージサイズが小さいため、高速で効率的に処理できます。また応答をキャッシュできる為、サーバーはデータをキャッシュに保存して、ページの読み込み時間を短縮できます。
#### 1.b RESTのデメリット
RESTにはプロコトルの規定があり、https上でしか動作しません。また、RESTは設計思想の一つであり厳格な規定が存在しない為、**人によって記述方法が異なる**というケースが生じてしまい、中身が分かりにくくなってしまうというデメリットがあります。
### 2.SOAPapi
*Simple Object Access Protocol*の略である。

SOAP は独立しており、どのトランスポートプロトコルでも動作する。

チームが使用するアプリケーション間の通信のためのインターフェースとして機能します。

%*1%{#ff0000}https://ics.uci.edu/~fielding/pubs/dissertation/top.htm



