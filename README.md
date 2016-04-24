# jquery-environment
jQuery+各種ビルドツールのテンプレート

## 目的
jQueryに各種使えるビルドツールをまとめたもの。毎回Package.jsonとgulpfileを0から考えてしこしこ書きたくない。

# Write less,do more.

## usage
npmインタフェースでビルドプロセスを呼び出せるようにしています。  
gulpよくしらない+設定のことを意識せずに開発したい人向け。
##### 準備(このプロジェクトをクローンして最初に行う)
```shell
npm run prepare
```
##### ソースビルド
```shell
npm run build
```
##### 開発
```shell
npm run develop
```
上記コマンドが走っている状態でsrc/以下を編集すると自動的にビルド・ブラウザがリロードされて、  
変更を即座に確認できる。
## 構成
|ディレクトリ名|役割              |
|:------------:|:----------------:|
|src/htdocs    |htmlを配置        |
|src/scripts   |jsファイルを配置  |
|src/scss      |scssファイルを配置|

### 使用プラグイン説明

##### gulp-concat
browserifyやWebpackなど選択肢はありますが、どうもjQueryの「グローバル変数にプラグインを突っ込むことで依存関係を管理する」
方式とCommonJS方式の折り合いが難しいので、思い切ってgulp-concatで「全部のファイルを一つに連結するだけ」という管理方法にしてみました。  
Webpack.config.jsをいじることでうまくCommonJSスタイルと旧来のjQueryスタイルを両立できるのかもしれませんが、おそらくWebpack.config.jsが秘伝のタレ化する気がします...

##### gulp-babel
gulp-concatを使っているのでrequire()は使用できませんが、ES6のクラス構文やテンプレートリテラル、アロー式は使えると捗るので使用しています。

### 推奨コードスタイル
今までのjQueryの書き方に、ちょくちょくES6方式の書き方を混ぜていくくらいの書き方のほうが安定するかも
