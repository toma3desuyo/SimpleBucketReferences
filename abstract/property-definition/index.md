# プロパティの定義

## 概要
オブジェクトにフィールドやアクセサを設け、外部からの取得・設定を可能にする。

## 振る舞い
読み取り専用にしたい場合は setter を用意しないか不変の値を返す。遅延計算プロパティはキャッシュの有無を説明する。

## 例
class User:
  function init(name):
    self.name = name
  function rename(new_name):
    require(non_empty(new_name))
    self.name = new_name


## 注意点
直接フィールドを公開すると後で検証を挟みにくくなるので、アクセサ越しに統一する。
