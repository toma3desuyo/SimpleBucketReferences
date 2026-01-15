# リストへの存在確認

## 概要
リストに指定要素が含まれているかを調べる。

## 振る舞い
非整列なら線形探索、整列済みなら二分探索が使える。等価比較の基準（値か同一性か）を決める。

## 例
function contains(list, value):
  for each item in list:
    if item == value:
      return true
  return false


## 注意点
NaN やオブジェクト参照など比較規則が特殊な値の扱いを確認する。
