# クラス

## 概要
データとそれを操作するメソッドをまとめた抽象。インスタンスごとに状態を持ち、共通の振る舞いを共有する。

## 振る舞い
コンストラクタで必須情報を受け取り、不変条件を満たすように初期化する。公開メソッドだけが外部から状態を変えられるよう可視性を制御する。

## 例
class Account:
  function init(owner, balance):
    require(balance >= 0)
    self.owner = owner
    self.balance = balance
  function deposit(amount):
    require(amount > 0)
    self.balance += amount


## 注意点
状態を持たない処理は静的関数として切り出すとテストしやすい。
