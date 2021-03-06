# homepage
筑波大学システム情報の佐野研究室のHPです

## 開発環境
このHPの開発はは以下のプログラミング言語等によって構成されてます。<br>

- HTML / CSS <br>
- JavaScript (Vue.js, Nuxt.js) <br>
- Git / GitHub <br> 

もしこれらの知識が欠けている場合には初心者用に<strong>学習すべき[ロードマップ](https://github.com/ZeroSano/homepage/blob/master/static/sanolab/webサイトtutorial.pptx) </strong>を簡易的ですが作成しました。これらを参考にしながら進めていくと可能な限り最小時間でcatch up ができると信じています。


## Setup

### 開発の流れ
このHPはGitHubで管理されて開発されています。今回はGitHubでの開発に不慣れな人向けに、簡単に開発環境の流れを紹介します。<br>
大まかな流れとしては

1. ローカルにコードを持ってくる（1回目のみ）
2. 必要なパッケージ等をインストールする（1回目のみ）
3. git でブランチを切り替える
4. 変更・追加したい部分を編集
5. gitでpull requestを作成

です。もしgit について不安がある場合は[ロードマップ](https://github.com/ZeroSano/homepage/blob/master/static/sanolab/webサイトtutorial.pptx)でも何かwebサイトを通じてでも、``` git add , commit, push, branch ```について調べてみてください。
s
実際に動かすコマンドとしては以下の通りです。

まず1回目のみローカル（自分のPC）に作業するための環境を構築します
```bash
# 1. ローカルにコードを持ってくる（1回目のみ）
$ git clone https://github.com/ZeroSano/homepage.git

# 2. 必要なパッケージ等をインストールする（1回目のみ）
$ cd homepage # 作業ディレクトリに移動
$ npm install # 必要なパッケージを一括してインストール
```
これで作業環境構築が完了です。

次にgitでブランチを作成しながら開発していきます。$ の隣に書いてあるコードをterminal等で打っていきます。
```bash
# まずmasterブランチにて最新の状態にアップデートします
$ git branch 
>> * master # ←のように返答があればOK。今masterブランチにいることを確認してください
$ git pull # 差分があれば更新されたものが降ってきてあなたのmasterブランチが最新のものになります。

# 3. git でブランチを切り替える（以下ではsample_branchを任意のブランチ名に変更してください）
$ git branch sample_branch # sample_branchというブランチを作成します
$ git checkout sample_branch # ブランチをsample_branchに移動します

# 4. 変更・追加したい部分を編集
$ npm run dev (これでhttp://localhost:3000/homepage/　であなたの開発環境をサイト上で見れます)

# gitで変更したいファイルを選択（ステージング）
$ git add . # ここでは全てのファイルを閃t無くしています

# 変更分をコミットしていきます
$ git commit -m "任意のメッセージをここに書いてください"

# 5. gitでpull requestを作成
git pull origin sample_branch
```
最後にgithubのページにてポチポチっとpull requestを作成してください。

以上がブランチを切って開発する流れになります。必ずブランチを切る際にはmasterブランチで```git pull```をして最新の状態にしてから作業を行うようにしてください。

また、ブランチがいらなくなったら```git branch -D sample_branch```でsample_branchのブランチを消すとことができます。


### デプロイ
現時点（2021-03-10）ではCI / CD は作成していません。 また [push-dir package] (https://github.com/L33T-KR3W/push-dir) でデプロイし、[Github Pages] (https://pages.github.com/)でホスティングしています。 そのため、ローカルでの変更を直接サイトに変更させたい場合には以下の手順でコマンドを打ってください。

```bash
# masterブランチに移動します。
$ git checkout master

# gitでコミット
$ e.g., git add .
$ e.g., git commit -m 'xxxx'

# 公開する用のページを作成します
$ npm run generate

# push-dirをつかってWEBに公開します
$ npm run deploy
```
``` npm run generate / deploy```の部分だけでいいんじゃないかとか思うかもしれませんが、毎回gitにてコミットしないとうまくいかないので上記の流れに気をつけてください。
