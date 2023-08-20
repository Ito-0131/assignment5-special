# 特別課題

### URLとは
"URL"とは「Uniform Resource Locator」の略称で、インターネット上のリソース（データやサービス）を特定するための形式的な表示方法です。
### クエリ文字列とは
クエリ文字列は、ウェブページのURLに追加されるパラメータのことを指します。ウェブサーバーに情報を送信するために使用される文字列で、一般的なクエリ文字列の形式は、URLの末尾に「?」を記述し、その後にパラメータ名と値のペアを続けて記述します。パラメータ名と値は「=」で区切り、複数のパラメータは「&」で区切ります。

基本のURLが” https://example.com "だとすると、基本のURLにクエリ文字列を追加すると" https://example.com/?query=keyword&category=1234 "のようになります。

≪参考文献≫https://online.dhw.co.jp/kuritama/query-string/

### パスパラメータとは
ホスト名(「://」から次の「/」までの間)から「?」までの部分。パスパラメータは、URLの住所の一部で、ウェブページ内の特定の部分を示します。
「 https://example.com/users/ 」というURLでは、最後の「users」がパスパラメータです。


・**クエリ文字列との違いについて**

パスパラメータはURLの一部に情報を埋め込む方法で、特定のリソースを識別するために使用されます。例えば、ユーザーIDを使って特定のユーザー情報を表示する場合などです。

一方、クエリ文字列はURLの末尾に「?」から始まるパラメータを追加する方法で、検索条件やフィルタリングを行うために使用されます。パラメータと値を?以降の形式で指定します。オプションのパラメータや検索条件、ソート、ページングのような動的な情報を伝えるために使用されます。


### HTTPメソッドとは
1. GET

GETメソッドは要求する情報をURLのクエリパラメータとして送信され、データを取得するために使用するメソッドです。サーバーに情報の取得を要求するだけで、サーバー側のデータは変更されません。また、URLに制限があるため、データのサイズに制約があります。

1. POST

POSTメソッドとは、HTTP通信でクライアント（Webブラウザなど）からWebサーバへ送るリクエストの種類の一つです。サーバーに対して情報の追加や更新など、データの変更を要求することができます。データをHTTPリクエストのボディに含めて送信します。データは暗号化されず、URLには表示されません。また、データのサイズに制限がなく、大量のデータを送信することができます。

1. PUT

HTTPを通じてサーバに対してリソース（ファイルなど）の追加あるいは更新を指示するためのメソッドで、指定のリソースが存在しない場合は新規に作成し、すでに存在する場合は送信したデータで上書きします。たとえば、ユーザーアカウント情報の更新、記事の編集、データの上書きなどに使用します。注意する点としては、部分的な更新ではなく、完全なリプレース（置換）が行われることです。ボディに含めるデータは、更新すべきリソースの新しいデータで置き換えるため、リソース全体を送信する必要があります。

1. PATCH

PUTと同じくデータを更新するメソッドですが、少し意味合いが異なります。PUTがデータの完全な更新やリソースの作成などに使用されルのに対し、PATCHは記事の一部分の修正やプロフィール情報の一部の変更などデータの一部を更新することを目的としています。

1. DELETE









