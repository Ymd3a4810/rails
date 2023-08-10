# 8/4
## 1. node jsのバージョンを管理するツール
https://qiita.com/heppokofrontend/items/5c4cc738c5239f4afe02
リポジトリごとに違うバージョンを使うのが当たり前

### 2. 1 node-envを入れる
https://github.com/nodenv/nodenv
1. `brew install nodenv`
2. `brew upgrade nodenv node-build`
3. 現在のシェルを確認 `echo $SHELL`
4. `cd ~`をして`ls -al`
5. `$(nodenv init -)`を.zshrcについか
`vi .zshrc`

### 2.2 node-envを使う
https://zenn.dev/donchan922/articles/b08a66cf3cbbc5
1. バージョン確認 `nodenv versions`
2. `nodenv install -l | grep 14`
3. 14のインストール `nodenv install 14.21.3`
4. 14を使う `nodenv local 14.21.3`
5. `.node-version`というファイルが上記のコマンドを実行後に作成されるので、コミットする

### topコマンドでPCの監視をする
サーバーサイドエンジニアはサーバーのパフォーマンス監視も行います
MACでも自分のPCの状態を監視できるので覚えて置きましょう
https://atmarkit.itmedia.co.jp/ait/articles/1706/30/news018.html

## 2. Webpackerを動かすには
`rails s`だけだと、webpackerがbuildが自動で行われないので、

### 2.1. webpacker => Railsにライブラリとしてバインドされてるやつ(今使っている方)
`rails webpacker:install`
`bin/rails webpacker:compile`

`Webpacker::Manigest::MissingEntryError`
https://wild-outdoorlife.com/ruby-on-rails/webpack5-error/

### 2.2 webpack => Railsとは別にインストールしていやつ
`bin/webpack-dev-server`を別に起動する必要がある

https://qiita.com/ahuiru/items/062bbc1b351819a3eeb8



8/3
https://diver.diveintocode.jp/dive_into_course/web_engineer_step_up/curriculums/2306

app/assets: HTML, CSS, 画像などの「アセットファイル」が置かれる。
app/controllers: コントローラが置かれる。
app/javascript: JavaScriptファイルが置かれる。
app/models: モデルが置かれる。
app/views: ビューテンプレートが置かれる。
bin: railsコマンドなどの実行ファイル（コマンドを実行した時に呼ばれる、実際に実行する処理を定義したプログラム）が置かれる。
config: アプリの設定ファイルが置かれる。データベースとの接続に使う情報や、ルーティングなど。
db: データベースそのものに関するファイルが置かれる。現時点でのデータベース構造や、データベース構造に変更を加えるためのマイグレーションファイルなど。
log: アプリの動作ログが書き込まれるファイルが置かれる。
public: 静的なファイルが置かれる。HTMLページや画像など。app/assetsとは異なり、リクエストを受けて動的に加工して配信するものではなく、そのまま返せる状態のものが置かれる。
test: アプリの動作をテストするためのプログラムや、テスト用のデータを定義するプログラムが置かれる。
テスト用のフレームワークにRSpecを使う場合、testではなくspecというディレクトリを利用することになる

# MVC
https://diver.diveintocode.jp/dive_into_course/web_engineer_step_up/curriculums/2487
MVCとは、アプリケーションの役割分担方式のひとつの形
Model：データベースの操作やデータの計算などを受け持つ。
View：ユーザが見る画面への出力を担う。HTMLを生成する。
Controller：ModelとViewの間を取り持つ。例えば、ユーザから送信された値を受け取ってModelに渡したり、Modelから受け取った処理結果をViewに渡すなど。
アプリケーションが満たすべき機能をModel, View, Controllerの概念で捉え直し、それに則ってコードを分割する手法

# index, showアクションの処理の流れ
https://diver.diveintocode.jp/dive_into_course/web_engineer_step_up/curriculums/2325
アプリケーションの基本機能であるレコードの「作成（Create）」「読み込み（Read）」「更新（Update）」「削除（Delete）」
<% %>というタグ→テンプレートエンジンerbの機能です。<% %>で囲んだ中をRubyのコードと解釈しRubyが実行
# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
