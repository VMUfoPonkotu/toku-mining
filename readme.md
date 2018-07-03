# 必要環境
node.js v8.11.3(async-await使えるなら何でも)

# 機能概要
般若心経を1秒に1回転させ、徳をジェネレートするプログラムです。  
(process.json内のTIMEOUT(ミリ秒指定)の値を変更する事で、1回転に必要な秒数を変更可能)

# 環境設定
## windows環境
[Node.js公式サイト](https://nodejs.org/ja/)より最新LTS版のインストーラーを取得し、インストール。  
インストール後、コンソールから npm install -g pm2 コマンドを実行、nodeのプロセスマネージャーをインストール。  
## linux環境
任意の方法でnodeのインストールを実行する。nvmとかnodebrewとか使おう。  
インストール後、コンソールから npm install -g pm2 コマンドを実行、nodeのプロセスマネージャーをインストール。  

# 実行方法
toku-miningディレクトリ以下で pm2 start process.json コマンドを実行。  
(windows用にstart.batを用意してるので、それ実行しても大丈夫です。ちゃんと中身見てから実行してね)

# 終了方法
pm2 kill allでプロセス終了。

# 応用
## 自動起動
windowsの場合、start.batのショートカットを作り、スタートアップフォルダ(わかんなかったらググってね)に入れておくと、windows起動時に徳マイニングが実行されます。
## 任意のテキストでマイニングする
lib/chant.txtの中身を任意のテキストに書き換える事で、好きなテキストを回転させる事ができます。  
ルイズコピペとか回しとくと、何らかのエネルギー発生しそうだよね。
