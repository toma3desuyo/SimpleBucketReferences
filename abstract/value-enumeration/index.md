# 値の一覧取得

## 概要
連想配列から値だけを列挙する。キーは含まれないため重複値もそのまま並ぶ。

## 振る舞い
返される値が参照かコピーかを明示する。ミュータブルな値を参照で返すと外部から内部が変更される。

## 例
function values(map):
  list = []
  for each pair in map:
    list.append(pair.value)
  return list


## 注意点
順序保証や反復中の変更可否を仕様に書いておく。
