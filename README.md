# homepage
筑波大学システム情報の佐野研究室のHPです

## 開発環境
このHPの開発はは以下のプログラミング言語等によって構成されてます。<br>

- HTML / CSS <br>
- JavaScript (Vue.js, Nuxt.js) <br>
- Git / GitHub <br> 

もしこれらの知識が欠けている場合には初心者用に<strong>学習すべき[ロードマップ](https://github.com/ZeroSano/homepage/blob/master/static/sanolab/webサイトtutorial.pptx) </strong>を簡易的ですが作成しました。これらを参考にしながら進めていくと可能な限り最小時間でcatch up ができると信じています。


## Build Setup

### 開発の流れ
このHPはGitHubで管理されて開発されています。今回はGitHubでの開発に不慣れな人向けに、簡単に開発環境の流れを紹介します。<br>
大まかな流れとしては

1. ローカルにコードを持ってくる
2. 必要なパッケージ等をインストールする
3. git でブランチを切り替える
4. 変更・追加したい部分を編集
5. gitでpull requestを作成

です。もしgit について不安がある場合は[ロードマップ](https://github.com/ZeroSano/homepage/blob/master/static/sanolab/webサイトtutorial.pptx)でも何かwebサイトを通じてでも、``` git add , commit, push, branch ```について調べてみてください。
実際に動かすコマンドとしては以下の通りです。

```bash
# 1. ローカルにコードを持ってくる
$ git clone https://github.com/ZeroSano/homepage.git

# 2. 必要なパッケージ等をインストールする
$ cd homepage && npm install

# 3. git でブランチを切り替える
$ git checkout -b {任意のブランチ}

# 4. 変更・追加したい部分を編集
$ npm run dev (これでhttp://localhost:3000/homepage/　であなたの開発環境をサイト上で見れます)

# 5. gitでpull requestを作成
分からなければ自身で「git プルリク」のように調べてみてください

```

### デプロイ
現時点（2021-03-10）ではCI / CD は作成していません。 また [push-dir package] (https://github.com/L33T-KR3W/push-dir) でデプロイし、[Github Pages] (https://pages.github.com/)でホスティングしています。 そのため、ローカルでの変更を直接サイトに変更させたい場合には以下の手順でコマンドを打ってください。

```bash
# gitでコミット
$ e.g., git add .
$ e.g., git commit -m 'xxxx'

# 公開する用のページを作成します
$ npm run generate

# push-dirをつかってWEBに公開します
$ npm run deploy
```
``` npm run generate / deploy```の部分だけでいいんじゃないかとか思うかもしれませんが、毎回gitにてコミットしないとうまくいかないので上記の流れに気をつけてください。
