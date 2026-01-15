# リスト

## 概要
順序付きで可変のシーケンス。インデックスアクセスと挿入・削除ができる。

## 振る舞い
末尾追加は多くの実装で amortized O(1)。先頭挿入は O(n) になることが多い。

## 例
function append(list, value):
  list.push(value)
  return list


## 注意点
異なる型を混在させるかどうかは事前に方針を決める。
