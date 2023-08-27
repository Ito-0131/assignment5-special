# 特別課題

### URLとは
"URL"とは「Uniform Resource Locator」の略称で、インターネット上のリソース（データやサービス）を特定するための形式的な表示方法です。
***

### クエリ文字列とは
クエリ文字列は、ウェブページのURLに追加されるパラメータのことを指します。ウェブサーバーに情報を送信するために使用される文字列で、一般的なクエリ文字列の形式は、URLの末尾に「?」を記述し、その後にパラメータ名と値のペアを続けて記述します。パラメータ名と値は「=」で区切り、複数のパラメータは「&」で区切ります。

基本のURLが” https://example.com "だとすると、基本のURLにクエリ文字列を追加すると" https://example.com/?query=keyword&category=1234 "のようになります。

≪参考文献≫https://online.dhw.co.jp/kuritama/query-string/

### パスパラメータとは
ホスト名(「://」から次の「/」までの間)から「?」までの部分。パスパラメータは、URLの住所の一部で、ウェブページ内の特定の部分を示します。
「 https://example.com/users/ 」というURLでは、最後の「users」がパスパラメータです。

***
・**クエリ文字列との違いについて**

パスパラメータはURLの一部に情報を埋め込む方法で、特定のリソースを識別するために使用されます。例えば、ユーザーIDを使って特定のユーザー情報を表示する場合などです。

一方、クエリ文字列はURLの末尾に「?」から始まるパラメータを追加する方法で、検索条件やフィルタリングを行うために使用されます。パラメータと値を?以降の形式で指定します。オプションのパラメータや検索条件、ソート、ページングのような動的な情報を伝えるために使用されます。

***
### HTTPメソッドとは
1. GET

GETメソッドは要求する情報をURLのクエリパラメータとして送信され、データを取得するために使用するメソッドです。サーバーに情報の取得を要求するだけで、サーバー側のデータは変更されません。また、URLに制限があるため、データのサイズに制約があります。

2. POST

POSTメソッドとは、HTTP通信でクライアント（Webブラウザなど）からWebサーバへ送るリクエストの種類の一つです。サーバーに対して情報の追加や更新など、データの変更を要求することができます。データをHTTPリクエストのボディに含めて送信します。データは暗号化されず、URLには表示されません。また、データのサイズに制限がなく、大量のデータを送信することができます。

3. PUT

HTTPを通じてサーバに対してリソース（ファイルなど）の追加あるいは更新を指示するためのメソッドで、指定のリソースが存在しない場合は新規に作成し、すでに存在する場合は送信したデータで上書きします。たとえば、ユーザーアカウント情報の更新、記事の編集、データの上書きなどに使用します。注意する点としては、部分的な更新ではなく、完全なリプレース（置換）が行われることです。ボディに含めるデータは、更新すべきリソースの新しいデータで置き換えるため、リソース全体を送信する必要があります。

4. PATCH

PUTと同じくデータを更新するメソッドですが、少し意味合いが異なります。PUTがデータの完全な更新やリソースの作成などに使用されルのに対し、PATCHは記事の一部分の修正やプロフィール情報の一部の変更などデータの一部を更新することを目的としています。

5. DELETE

DELETEメソッドを使用すると、指定したURLのリソースが完全に削除されます。削除後は、そのリソースは利用できなくなります。
DELETEメソッドは、リソースを削除するために使用されます。例えば、ユーザーアカウントの削除、記事の削除、ファイルの削除などに使用します。
リクエストURLには、削除したいリソースの識別子（一意のIDなど）を指定します。

***
### HTTPステータスコードとは何か

・200  
リクエストは正しく処理され、要求された内容が返信されています。ブラウザ上でPCやスマホの画面で正しくサイトが閲覧できる際には、この数字が返ってきています。  

・201  
リクエストは成功し、新規で作成されたリソースのURLが返信されています。
例えば、PUTメソッドでリソースを指定し作成しようした際に、そのリクエストを行って、サーバ側も受理して作成も完了した場合に返される状態がこのステータスになります。    

・400  
クライアントのリクエストが不正であることを示します。ブラウザか端末に問題があることがあり、対処方法としてはブラウザを変更する、パソコンを変えてみる、スマートフォンでアクセスする、キャッシュやcookieを削除したりする方法があります  
 
 ・404  
リクエストされたリソースが存在しないことを示します。原因はURLのスペルが間違っていることや、リダイレクトの設定が間違っていることなどURLに関係する    

・500  
サーバ内部で何らかのエラーが発生したことを示します。具体的なエラーの詳細が表示されないことがあり、頻繁に遭遇するエラーコードの一つです。考えられる原因はさまざまで、バグ、リソース不足、データベースの接続エラーなどがあります。ウェブサーバやアプリケーションサーバ内部の問題なので、クライアントが行う操作で解決することはできません。

***
### リクエストヘッダーとは何か
サーバーに対してクライアントの要求や状態を伝えるために使用されます。リクエストヘッダーの主なフィールドとしては、
User-Agent（ユーザーエージェント）、Accept（受け入れ）、Content-Type（コンテンツタイプ）、Authorization（認証）、Cookie（クッキー）、Referer（リファラ）などがあります。  

### リクエストボディとは何か
クライアントがサーバーに送信するHTTPリクエストの一部であり、主にデータや情報を含んでいます。フォームデータ、JSONデータ、画像や動画ファイルなど、さまざまな形式のデータを含めることができます。

***
### レスポンスヘッダーとは何か
サーバーがクライアント（ブラウザなど）に対して送信する情報です。送信される情報としては、レスポンスのステータスコードやサーバーのバージョン、セキュリティ関連の情報などが含まれます。  

### レスポンスボディとは何か
レスポンスボディは、ウェブサーバーがクライアント（ブラウザなど）に送信する実際のデータやコンテンツのことを指します。Webブラウザで特定のウェブサイトにアクセスすると、ウェブサーバーはレスポンスボディとしてそのウェブページのHTML形式のテキストデータが記述されます。
***
### JSONとは何か  
JSONはと「JavaScript Object Notation」の略称です。  
”JavaScript”はプログラミング言語の一つであり、"Object Notation" はデータを表現する際の構文や文法のルールを表しています。

特徴としてはテキスト形式で可読性が高い、単純で軽量なこと、コンピュータから見た場合にも決まった形式に沿って記述されているため読み込んだり加工したりしやすい構造であるなどが挙げられます。

テキストベースであるXML (Extensible Markup Language)と比べてもよりシンプルであり、 各種言語との親和性も高く使い勝手も良いことから、Webアプリケーションやモバイルアプリケーションなど、さまざまなプログラムでデータのやり取りに利用されています。

[参考サイト](https://cloudapi.kddi-web.com/magazine/json-javascript-object-notation){:target="_blank"}
***
### HTTPSとHTTPの違い
HTTPS（HyperText Transfer Protocol Secure）とHTTP（HyperText Transfer Protocol）は、インターネット上で情報をやり取りする際に使用されるプロトコルです。

HTTPSにはセキュリティ証明書が使用されており、Webサイトの信頼性を示す情報が含まれています。一方で、HTTPでは証明証が使用されておらず、Webサイトの信頼性を示す手段がありません。
HTTPSは通信内容が暗号化されるのでデータの盗聴やなりすましを防ぐことができますが、HTTPは暗号化されていないためセキュリティの面で脆弱性があります。
***

### JSONのサンプルコード
```JSON
"UserInfo" : [  
{ "id" : 1,  "name" : "Matsumoto", "age" : 27 },  
{ "id" : 2,  "name" :"Hamada", "age" : 35},  
{ "id" : 3,  "name" : "Endo", "age" : 42 }  
   ]
```
