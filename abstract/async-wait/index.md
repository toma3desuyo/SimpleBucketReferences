# 非同期の待機

## 概要
非同期タスクの完了を待って結果を受け取る操作。

## 振る舞い
待機中にスレッドをブロックしない仕組みを使う。タイムアウト時の後処理やキャンセルの伝播を決める。

## 例
function wait(task, timeout):
  result = task.await(timeout)
  if result.timed_out:
    raise Error("timeout")
  return result.value


## 注意点
未完了タスクをどう扱うかを決め、リークを防ぐ。
