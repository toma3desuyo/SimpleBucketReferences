# 要素数の取得

## 概要
コレクションに含まれる要素数を調べる操作。配列や固定長構造では O(1)、ストリームでは全走査が必要になる。

## 振る舞い
反復を消費するイテレータ型では長さ取得が一度きりになることがある。コストの大きさをドキュメントで明示する。

## 例
function length_of(collection):
  if collection.has_constant_length:
    return collection.length
  count = 0
  for each _ in collection:
    count += 1
  return count


## 注意点
文字列長はコードポイント基準かコードユニット基準かで結果が変わるため、基準を合わせる。
