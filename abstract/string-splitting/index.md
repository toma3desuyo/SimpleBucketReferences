# 文字列の分割

## 概要
区切り文字やパターンを基準に文字列を複数の部分に分ける。

## 振る舞い
区切りが連続したときに空要素を残すか捨てるか、最大分割数をどう扱うかを仕様に合わせる。

## 例
function split(text, delimiter, max_parts=None):
  parts = []
  cursor = 0
  while max_parts is None or length(parts) < max_parts - 1:
    pos = find(text, delimiter, cursor)
    if pos < 0: break
    parts.append(slice(text, cursor, pos))
    cursor = pos + length(delimiter)
  parts.append(slice(text, cursor))
  return parts


## 注意点
正規表現で区切ると空文字一致が起きる場合があるので注意。
