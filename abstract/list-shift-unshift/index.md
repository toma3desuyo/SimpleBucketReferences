# 先頭の要素追加 / 削除

## 概要
リストの先頭に挿入（unshift）し、先頭から取り出す（shift）操作。キューの実装で使う。

## 振る舞い
動的配列では再配置が発生し O(n) になりやすい。頻用するならデックやリンクリストを選ぶ。

## 例
function queue_ops(queue, value):
  queue.unshift(value)
  return queue.shift()


## 注意点
空のときの挙動を決め、並行アクセスではロックなどで競合を防ぐ。
