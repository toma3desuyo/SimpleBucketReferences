# 連想配列の要素削除

## 概要
指定キーの要素をマップから取り除く。

## 振る舞い
存在しないキーを指定したときの扱い（無視/例外）を決める。走査中の削除はイテレータ規約に従う。

## 例
function remove(map, key):
  if not map.contains(key):
    raise Error("missing")
  map.delete(key)


## 注意点
弱参照マップではガーベジコレクションに任せるケースもある。
