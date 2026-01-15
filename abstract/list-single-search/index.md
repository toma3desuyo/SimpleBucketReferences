# リスト内の単一検索

## 概要
リストから条件に合う最初の要素を取得する。

## 振る舞い
線形探索で O(n)。整列済みなら二分探索で高速化できる。見つからない場合の戻り値を統一する。

## 例
function find_first(list, predicate):
  for each item in list:
    if predicate(item):
      return item
  raise Error("not found")


## 注意点
複数一致がある場合は最初を返すことを明記する。
