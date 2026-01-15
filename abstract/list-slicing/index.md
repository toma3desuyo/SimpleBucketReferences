# リストの部分抽出

## 概要
開始位置と終了位置を指定して連続した要素を取り出す。多くは元のリストを変更せず新しいリストを返す。

## 振る舞い
範囲外は切り詰めるか例外にするかを決める。負のインデックスを許すかどうかも仕様で揃える。

## 例
function slice(list, start, end):
  result = []
  i = max(0, start)
  while i < end and i < length(list):
    result.append(list[i])
    i += 1
  return result


## 注意点
ビューを返す実装では元リストの変更が結果に反映されることを伝える。
