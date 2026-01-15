# 末尾の要素追加 / 削除

## 概要
リスト末尾への追加(push)と末尾からの取り出し(pop)を行う。スタック操作の基本。

## 振る舞い
動的配列では amortized O(1)。空リストで pop したときの挙動（例外/特別値）を決める。

## 例
function push_pop(stack, value):
  stack.push(value)
  return stack.pop()


## 注意点
スレッドセーフにしたい場合はロックやロックフリー構造を利用する。
