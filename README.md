# jquery-environment
jQuery+各種ビルドツールのテンプレート

## 目的
jQueryに各種使えるビルドツールをまとめたもの。毎回Package.jsonとgulpfileを0から考えてしこしこ書きたくない。

# Write less,do more.

## usage
準備(このプロジェクトをクローンして最初に行う)
```shell
npm run prepare
```
ソースビルド
```shell
npm run build
```
開発
```shell
npm run develop
```
上記コマンドが走っている状態でsrc/以下を編集すると自動的にビルド・ブラウザがリロードされて、  
変更を即座に確認できる。
## 構成
|ディレクトリ名|役割|h
|src/htdocs|htmlを配置|
|src/scripts|jsファイルを配置|
|src/scss|scssファイルを配置|

### 使用プラグイン


### 推奨コードスタイル
