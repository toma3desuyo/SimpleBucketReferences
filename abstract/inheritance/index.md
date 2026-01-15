# 継承

## 概要
親クラスの性質や振る舞いを子クラスが引き継ぎ、必要に応じて拡張・上書きする仕組み。

## 振る舞い
共通処理は親に置き、子は差分だけを書く。オーバーライド時は親の契約を破らない。

## 例
class Animal:
  function speak(): return "..."
class Dog extends Animal:
  function speak(): return "bark"


## 注意点
階層が深くなると追跡が難しくなるので、合成や委譲も検討する。
