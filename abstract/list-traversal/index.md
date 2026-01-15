# リストの全走査

## 概要
リストの全要素を順に処理する。

## 振る舞い
反復回数は長さに比例し O(n)。走査中の追加・削除は順序を乱すことがあるので避ける。

## 例
function traverse(list, action):
  for each item in list:
    action(item)


## 注意点
重い処理はバッチ化するか途中で中断できるよう設計する。
