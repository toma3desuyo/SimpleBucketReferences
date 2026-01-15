# コールバック関数

## 概要
処理完了時に呼び出される関数。イベントや非同期結果の受け取りに使う。

## 振る舞い
何回呼ばれるか、エラーはどう渡すかなど契約を決める。コールバック内での例外がどこへ伝わるかを揃える。

## 例
function do_async(task, callback):
  try:
    result = task()
    callback(result, null)
  catch err:
    callback(null, err)


## 注意点
ネストが深くなると読みにくいので、Promise/Futureなど合成しやすい抽象を検討する。
