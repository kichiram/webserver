# WEBサーバ勉強会
アジェンダ
* WEBサーバとは
* 一般的に利用されているwebサーバ
* webサーバの仕組み
* TLS（SSL）とは
* おまけ

## WEBサーバとは
- URL (Webアドレス) および HTTP (ブラウザーがWebページを閲覧するためのプロトコル) を理解するソフトウェアのことです。格納しているWebサイトのドメイン名 (mozilla.org など) を通してアクセスすることができ、コンテンツをエンドユーザーの端末に配信します。
- 簡単に説明するとブラウザなどからのURLによるリクエストを受ける機能のこと。静的なコンテンツは単独でレスポンスを返せますが、動的なコンテンツはphpなどのプログラムと連携して結果を返します。

引用：https://developer.mozilla.org/ja/docs/Learn/Common_questions/What_is_a_web_server
## 一般的に利用されているwebサーバ
- Apache（アパッチ）
  - OSS（オープンソースソフトウェア）のWebサーバーで、正式名称は「Apache HTTP Server」です。
  - Apacheはマルチプロセッシングモジュールを採用しており、1つのスレッドごとに新しいプロセスを起動する方式です。動的なコンテンツの処理に適しており、CGIやPHPなどに向いています。
  - 扱うことのできる機能が豊富で、幅広い動作環境に対応していることが特徴
- Nginx（エンジンエックス）
  - Apache同様にOSS（オープンソースソフトウェア）。
  - Nginxはキャッシュサーバー不要でHTMLや画像などをキャッシュできるので、静的コンテンツを扱うのに適したWebサーバーといえます。
  - シングルスレッドを採用しており、1つのプロセスが複数の処理を行ないます。
  - 処理能力や同時接続数などの負荷への耐久力は、Apacheよりも高いといわれています。
- IIS（アイアイエス）
  - Windows用のWebサーバー機能です。Microsoft社が提供しているため、Windowsに特化しています。ApacheやNginxと違い、IISはOSSではありません。
  - IISはWindowsベースなので、情報表示においてグラフィックを多用しているので、命令文を入力して実行させるCUI（キャラクタ・ユーザ・インターフェース）よりも、直感的に操作可能なGUI（グラフィカル・ユーザ・インターフェース）である点も大きなメリットといえます。

引用：https://www.rworks.jp/system/system-column/sys-entry/16296/

## webサーバの仕組み
- IPアドレス、PORT、DHCP、DNS、MIME typeなどを交えて下記webサイトを利用して説明します。
  - [Webの仕組みとWebサーバの構造](https://atmarkit.itmedia.co.jp/ait/articles/0101/16/news003.html)

## TLS（SSL）とは
- セキュアなインターネット通信（https：//～）を行なう仕組みでデータを暗号化して送受信します。
  - 参考：https://www.infraexpert.com/study/security7.html

## おまけ
- golangならwebサーバ不要です。
  - 参考：https://qiita.com/rihofujino/items/39f1778d3458248e134d
