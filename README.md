# 概要

これはGoogleドキュメント（スプレッドシート）をつかって、Backlogへ課題を一括登録するツールです。

以下のような場合に、お使いいただけます。

* プロジェクト立ち上げ時に、定型のタスクを登録する必要があるとき
* 運用・保守など、定期的に同じタスクを行わなければならないとき

![](https://cacoo.com/diagrams/jv257uekYrdc9Uep-169AF.png)

# インストール

テンプレートとなるスプレッドシートを準備します。下記リンクをクリックして、スプレッドシートをコピーしてください。
* <a href="https://docs.google.com/spreadsheets/d/1BkQm3TD4BF0NuqGTQgW9jedFp1_QtcuDEYWCyQJ3s4c/copy" target="_blank">スプレッドシートをコピー(新しいタブで開いてください)</a>
* Googleにログインしていない場合、コピー時にエラーとなる場合があります。その際は、ログインして少し時間を置いてから再度お試しください。

# 入力項目について

テンプレートを元に、スプレッドシートの内容を登録したい情報に書き換えます。１行目のヘッダー行は、登録処理に必要な情報を含んでいるため、削除したり内容を変更しないようご注意ください。また「件名」「種別」は登録に必須となる項目ですので、必ず記入するようにしてください。

## 親課題
親課題が既に存在する場合は`課題キー`を指定してください。スプレッドシート内の課題を指定する場合は課題キーがまだ存在しないので、`*`を入力することで直近の親課題を指定していない課題を親課題とします。

# 実行方法

スプレッドシートを開いて10秒ほど待つと、スプレッドシートのメニューバーの一番右に「Backlog」というメニューが追加されているかと思います。  

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/menu.png)

実行には2ステップが必要です。以下の手順で実行してください。  
下記のような承認画面が出ることがあるかもしれませんが、こちらは”OK”を押して続行後、再度課題一括登録を実行してみてください。

![](https://cacoo.com/diagrams/jv257uekYrdc9Uep-D9EC2.png)


## STEP1: Backlogからデータを取得する
この手順では、Backlogに設定済みの定義(種別名、ユーザー名等)を取得します。

[Backlog]メニューから[STEP1:Backlogからデータを取得する]をクリックします。

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/menu_step1.png)

下記のような入力ダイアログが表示されますので、順に必要な情報を入力してください。
- BacklogのスペースID
- BacklogのAPIキー: https://backlog.com/ja/help/usersguide/personal-settings/userguide2378/
- 登録対象となるBacklogのプロジェクトキー

**デモ用Backlogプロジェクト**

お試しで使いたい方は [Backlogデモプロジェクト](https://demo.backlog.jp/) にて試すことができます。

* スペースID： `demo`.backlog.`jp`
* APIキー： `ShMb0ao0AQuwzysKGEvLu9kZ96UczRSUufi9dXVFTKAtIY4ODiljBnYs9SBBb1bj`
* プロジェクトキー： `STWK`


![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/form_step1.png)

上記情報を全て入力後、`実行`ボタンをクリックして定義一覧取得を実行します。  
正常に完了すると、右下に完了のポップアップが表示されます。

課題種別や、カテゴリーなど、必要な情報が選択できるようになっていることをご確認ください。

## スプレッドシートに課題を記入する

一括登録したい課題を1行に1課題ずつ入力してください。


## STEP2: 一括登録処理を実行する
[Backlog]メニューから[STEP2:課題一括登録を実行]をクリックします。

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/menu_step2.png)

下記のような入力ダイアログが表示されますが、`STEP1`で既に入力済みなので`実行`ボタンをクリックして一括登録処理を実行します。

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/form_step2.png)

登録処理実行時に、結果出力用のシートが新規作成され自動的にそのシートに遷移します。このシートで、一括登録された課題の（キー・件名）を一覧で確認することができます。

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/log_sheet.png)

![](https://github.com/nulab/backlog-template-issue-gas/wiki/images/result.png)

# 一度作ったスプレッドシートを再利用する場合

Backlog側のプロジェクト設定を変更しなければ、STEP2の操作だけで課題は登録されます。
もしも課題種別やカテゴリーなど、変更がある場合はSTEP1の操作から実行してください。
