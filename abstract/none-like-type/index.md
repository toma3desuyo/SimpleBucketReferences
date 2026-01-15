# 「ない」状態の型

## 概要
値が未指定であることを明示的に表すための型（None/Null/Option など）。

## 振る舞い
不在を返す理由をコメントで示し、呼び出し側が必ず分岐するよう型や慣習で強制する。

## 例
type Option<T> = Some(value:T) | None
function unwrap(opt):
  if opt is None:
    raise Error("value is absent")
  return opt.value


## 注意点
安易に None を返さず、ドメインで正当化できる場合だけ用いる。
