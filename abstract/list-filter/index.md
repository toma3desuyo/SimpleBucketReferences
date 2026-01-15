# リストへの条件フィルター

## 概要
条件を満たす要素だけを抽出して新しいリストを作る。

## 振る舞い
判定関数は真偽値を返し、副作用を避ける。元の順序を保つかどうかを仕様に合わせる。

## 例
function filter(list, predicate):
  result = []
  for each item in list:
    if predicate(item):
      result.append(item)
  return result


## 注意点
巨大データでは遅延フィルターやストリーミングを使い、メモリ使用量を抑える。
