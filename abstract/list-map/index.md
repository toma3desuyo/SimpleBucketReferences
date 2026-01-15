# リストの一括変換

## 概要
リストの各要素に同じ変換を適用し、新しいリストを得る。元のリストは変更しないのが基本。

## 振る舞い
変換関数は副作用を避ける。例外が発生した場合は途中までの結果を破棄するか、そのまま返すかを決める。

## 例
function map(list, transform):
  result = []
  for each item in list:
    result.append(transform(item))
  return result


## 注意点
重い処理ならバッチ化や並列化を検討し、順序保持の要否を明確にする。
