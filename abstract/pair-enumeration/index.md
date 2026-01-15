# 全ペアの取得

## 概要
連想配列などからキーと値の組を順に取り出す。

## 振る舞い
順序保証は実装依存。反復中に構造を変更すると結果が不定になる。

## 例
function entries(map):
  for each pair in map:
    yield (pair.key, pair.value)


## 注意点
大量データはイテレータで遅延提供し、一括リスト化を避ける。
